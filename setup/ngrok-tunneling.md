# Exposing Local Development to External Devices via ngrok

Tags: #ngrok #tunneling #mobile-testing #development
Level: Beginner
⏱️ Time: 10 min

## 🎯 Goal

Expose local development server to public internet. Test on mobile devices, share with teammates, demo to clients — all from local machine.

## 📋 Prerequisites

* **ngrok installed** (see Step 1)
* **ngrok account** (free tier works)
* **Local dev server running** (any language/framework)

## 🚀 Steps

### Step 1: Install ngrok

**Option A: Homebrew (macOS/Linux)**
```bash
brew install ngrok/ngrok/ngrok
```

**Option B: Manual Download**
1. Go to [ngrok.com/download](https://ngrok.com/download)
2. Download and extract
3. Move to PATH:
   ```bash
   sudo mv ngrok /usr/local/bin/
   ```

### Step 2: Configure Auth Token

1. Sign up at [ngrok.com](https://ngrok.com)
2. Get authtoken from dashboard
3. Link it:
   ```bash
   ngrok config add-authtoken <YOUR_AUTH_TOKEN>
   ```

### Step 3: Start Local Server

Run your dev server. Note the port.

| Stack      | Command                     |
|------------|----------------------------|
| .NET       | `dotnet run --launch-profile http` |
| Node.js    | `npm run dev`              |
| React/Vite | `npm run dev`              |
| Next.js    | `npm run dev`              |
| Python     | `python app.py` or `flask run` |
| Django     | `python manage.py runserver` |
| Go         | `go run main.go`           |
| PHP        | `php -S localhost:8000`    |

### Step 4: Create Tunnel

New terminal window:
```bash
ngrok http <PORT>
```

Example:
```bash
ngrok http 3000      # Node/React
ngrok http 5154      # .NET
ngrok http 8000      # Python/PHP
```

### Step 5: Access from Device

ngrok displays:
```
Forwarding    https://abc123.ngrok-free.app -> http://localhost:3000
```

Copy **https** URL. Open on phone/tablet.

## ⚙️ Common Port References

| Stack           | Default Port |
|-----------------|--------------|
| React (Vite)    | 5173         |
| Next.js         | 3000         |
| Create React App| 3000         |
| .NET (Kestrel)  | 5000/5154    |
| Express         | 3000         |
| Flask           | 5000         |
| Django          | 8000         |
| Vite dev server | 5173         |

## ⚡ Pro Tips

### Static Domain (Free)
1. Dashboard → Cloud Edge → Domains
2. Create free static domain
3. Use it:
   ```bash
   ngrok http 3000 --url your-name.ngrok-free.app
   ```

### Inspect Traffic
Visit `http://localhost:4040` while tunnel runs. See all requests, replay them.

### HTTPS Only
Always use `https://` URL. Modern mobile APIs require HTTPS (geolocation, camera, etc.).

## ⚠️ Common Issues

| Problem | Solution |
|---------|----------|
| "ngrok: command not found" | Verify installation. Check PATH. |
| Tunnel connects, page blank | Local server not running. Wrong port. |
| WebSocket fails | Use `ngrok http --log=debug` to diagnose. Some frameworks need WS-specific config. |
| URL changes every time | Claim static domain (see Pro Tips). |
| "Invalid authtoken" | Re-copy from dashboard. Check for trailing spaces. |

## 📚 References

* [Official ngrok docs](https://ngrok.com/docs)
* [ngrok agent options](https://ngrok.com/docs/agent)
