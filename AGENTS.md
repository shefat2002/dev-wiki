# 🤖 AGENTS.md

> Guidelines for humans and AI agents contributing to the **Dev Wiki** repository.

This document defines how content should be created, structured, and maintained to ensure consistency, clarity, and long-term usability.

---

# 🎯 Purpose

The goal of this repository is to build a **high-quality, practical, and scalable knowledge base** for software development.

Agents (human or AI) must:

* Produce **clear, actionable documentation**
* Follow a **consistent structure**
* Avoid unnecessary theory
* Focus on **real-world implementation**

---

# 🧠 Agent Responsibilities

When creating or updating content, an agent must:

### ✅ Do

* Write step-by-step guides
* Use simple and precise language
* Include code examples where helpful
* Add troubleshooting sections
* Keep content beginner-friendly when possible

### ❌ Avoid

* Theoretical explanations without application
* Ambiguous instructions
* Copy-pasting from external sources without adaptation
* Breaking the document structure

---

# 📁 File Placement Rules

Each document must be placed in the correct directory:

| Category                | Folder            |
| ----------------------- | ----------------- |
| Architecture & Design   | `architecture/`   |
| Environment Setup       | `setup/`          |
| Backend Development     | `backend/`        |
| Mobile Development      | `mobile/`         |
| Testing & QA            | `testing/`        |
| CI/CD                   | `cicd/`           |
| Infrastructure & DevOps | `infrastructure/` |

### Nested Structure (if needed)

* Tech-specific docs go inside subfolders
  Example:

  * `backend/dotnet/new-project.md`
  * `backend/node/express-setup.md`

---

# 📝 Document Naming Convention

Use **kebab-case** and descriptive names:

✅ Good:

* `setup-docker.md`
* `dotnet-authentication.md`
* `deploy-to-vps.md`

❌ Bad:

* `Doc1.md`
* `setupStuff.md`
* `final_version_latest.md`

---

# 📄 Required Document Structure

Every guide MUST follow this format:

```md
# [Task / Guide Title]

## 🎯 Goal
Explain what the guide accomplishes.

## 📋 Prerequisites
List required tools, accounts, or knowledge.

## 🚀 Steps
1. Step one
2. Step two
3. Step three

## ⚠️ Common Issues
- Problem → Solution

## 📚 References
- Official documentation links
```

---

# 🏷️ Metadata (Recommended)

At the top of each file, include:

```md
Tags: #docker #dotnet #backend  
Level: Beginner  
⏱️ Time: 10 min
```

---

# 💻 Code Guidelines

* Use proper markdown code blocks
* Mention language explicitly

Example:

```csharp
var builder = WebApplication.CreateBuilder(args);
```

* Keep code minimal and relevant
* Avoid unnecessary boilerplate

---

# 🖼️ Assets & Diagrams

* Store images in `assets/images/`
* Store diagrams in `assets/diagrams/`
* Use relative paths

Example:

```md
![Architecture](../assets/diagrams/api-flow.png)
```

* Prefer diagrams when explaining flows

---

# 🔁 Editing Existing Documents

When updating a document:

* Do NOT change structure unless necessary
* Improve clarity, not complexity
* Preserve original intent
* Update outdated steps

---

# 🔍 Content Quality Checklist

Before submitting, ensure:

* [ ] Title is clear and specific
* [ ] Steps are easy to follow
* [ ] No missing prerequisites
* [ ] Code is correct and tested (if possible)
* [ ] Includes troubleshooting section
* [ ] File is in correct folder

---

# 🤝 Pull Request Rules

* One topic per PR
* Use clear PR title:

  * `Add: Docker setup guide`
  * `Fix: Git workflow typo`
* Link related documents if applicable

---

# 🚀 AI Agent Behavior Rules

AI agents (ChatGPT, Copilot, etc.) must:

### ✔ Generate:

* Structured markdown
* Practical guides
* Clean formatting

### ❌ Must NOT:

* Hallucinate commands or APIs
* Add fake references
* Overcomplicate explanations

### ⚠ If unsure:

* Keep content generic but correct
* Add note: *"Verify with official docs if needed"*

---

# 🌟 Long-Term Vision

This repository should evolve into:

* A **developer handbook**
* A **team onboarding system**
* A **production-ready documentation hub**

Agents should always optimize for:

> Clarity > Simplicity > Practicality

---

# 📌 Final Rule

If a guide is not **immediately useful in real work**, it does not belong here.
