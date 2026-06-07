# TapTalk — MacBook setup (read this first)

GitHub is the source of truth: **https://github.com/CavenLink-Dev/TapTalk.v2**

---

## On your Mac — get the repo

### First time (no folder yet)

```bash
cd ~/Developer   # or wherever you keep projects
git clone https://github.com/CavenLink-Dev/TapTalk.v2.git
cd TapTalk.v2
```

### Already cloned before

```bash
cd TapTalk.v2
git pull origin main
```

Always run `git pull origin main` at the **start** of a Cursor session on either machine.

---

## Open in Cursor

1. **File → Open Folder** → select the `TapTalk.v2` folder
2. Cursor loads `.cursor/rules/taptalk-project.mdc` automatically every session (what TapTalk is + why)

---

## What is on GitHub (after latest push)

| Path | What it is |
|------|------------|
| `.cursor/rules/taptalk-project.mdc` | Always-on project context for Cursor AI |
| `MAC_HANDOFF.md` | This file |
| `DEV_ONLY_NO_AI.md` | Your personal checklist (not for AI) |
| `mulberry-symbols/` | AAC symbol SVG assets |

---

## Not on GitHub?

If you add files locally and do not push, your other machine will not get them. Run `git status` on Windows before leaving — anything untracked needs a **commit + push** or manual copy.

---

## Mac tools (when you start building in Phase 2)

Install when ready — no Expo app in the repo yet:

| Tool | Purpose |
|------|---------|
| [Cursor](https://cursor.com) | Editor |
| [Node.js LTS](https://nodejs.org) | Expo / React Native |
| Xcode (App Store) | iOS simulators optional; Expo Go on iPhone is primary |
| Expo Go on iPhone | Test on device (SDK 54) |
| Git | Usually pre-installed on Mac — `git --version` to check |

After the Expo project exists:

```bash
npm install
npx expo start
```

Scan QR with Expo Go on iPhone.

---

## End of every session (both machines)

```bash
git add .
git commit -m "Describe what you finished"
git push origin main
```

---

## Quick checklist — Mac arrival

- [ ] `git pull origin main` (or `git clone` if new)
- [ ] Confirm `mulberry-symbols/` folder is present
- [ ] Open folder in Cursor
- [ ] Continue from Phase 2 when ready

**Repo:** https://github.com/CavenLink-Dev/TapTalk.v2
