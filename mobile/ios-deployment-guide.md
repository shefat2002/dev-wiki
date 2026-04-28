# 📱 iOS Deployment Guide: Unity → App Store

This guide provides a complete step-by-step workflow for taking a Unity iOS game from development to release on the Apple App Store.

---

# 🚀 Phase 1: Apple Developer Portal Preparation

Before exporting from Unity, you must register your app in Apple’s ecosystem.

## 1. Register the App Identifier

1. Go to https://developer.apple.com  
2. Navigate to **Certificates, IDs & Profiles → Identifiers**
3. Click **+ (Add)**  
4. Select:
   - **App IDs → Continue**
   - **App → Continue**
5. Fill in:
   - **Description:** e.g. `500WhistlesRush`
   - **Bundle ID:** Select **Explicit**
   - Example: `com.mocciaart.500WhistlesRush`
6. Enable required **Capabilities**
7. Click **Register**

---

## 2. Create App Store Connect Record

1. Go to https://appstoreconnect.apple.com  
2. Navigate to **Apps → + → New App**
3. Fill in:
   - **Platform:** iOS
   - **App Name**
   - **Primary Language**
   - **Bundle ID**
   - **SKU**
4. Click **Create**

---

# 🎮 Phase 2: Unity Build Process

## 1. Configure Player Settings

- Bundle Identifier must match Apple portal
- Version: `1.0.0`
- Build Number: `1`

> ⚠️ Build number must be incremented for every upload.

---

## 2. Export the Project

- File → Build Settings → iOS → Build
- Choose an empty folder

---

# 📦 Phase 3: CocoaPods Integration

```bash
cd <your-unity-build-folder>
pod install
```

> ❌ Do NOT open `.xcodeproj`  
> ✅ Open `.xcworkspace`

---

# 🛠️ Phase 4: Xcode Archiving & Upload

- Open `Unity-iPhone.xcworkspace`
- Enable automatic signing
- Select Team

### Archive

Product → Archive

### Upload

Distribute App → TestFlight & App Store → Upload

---

# 🧪 Phase 5: TestFlight

- Wait for processing (10–30 min)
- Fix compliance if needed

### Testing
- Internal: team testing
- External: Apple review required

---

# 🏪 Phase 6: App Store Publishing

### Metadata
- Description
- Keywords

### Screenshots
- 1242 × 2688

### Submit
- Add build
- Add for review

---

# ✅ Final

App goes live after approval 🎉

---

# 📌 Flow

Unity → Build → Xcode → Upload → TestFlight → Submit → App Store
