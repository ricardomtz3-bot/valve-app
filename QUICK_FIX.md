# Quick Fix Checklist for Copilot Connection Issues

If you're having trouble connecting GitHub Copilot to VS Code, try these steps in order:

## 1. ✅ Basic Checks (Try First)

- [ ] **Restart VS Code** - Close and reopen VS Code completely
- [ ] **Check Copilot Icon** - Look at the bottom-right status bar for the Copilot icon
- [ ] **Verify Subscription** - Visit https://github.com/settings/copilot to confirm your subscription is active

## 2. 🔄 Sign Out and Sign In

```
1. Press Ctrl+Shift+P (Cmd+Shift+P on Mac)
2. Type: "GitHub Copilot: Sign Out"
3. Press Ctrl+Shift+P again
4. Type: "GitHub Copilot: Sign In"
5. Complete the browser authentication
```

## 3. 🔌 Check Extensions

- [ ] Open Extensions view (Ctrl+Shift+X / Cmd+Shift+X)
- [ ] Verify these are installed and enabled:
  - ✓ GitHub Copilot
  - ✓ GitHub Copilot Chat
- [ ] Update extensions to latest versions if needed

## 4. ⚙️ Verify Settings

Open Settings (Ctrl+, / Cmd+,) and check:

- [ ] **Editor: Inline Suggest Enabled** = ✓ Checked
- [ ] Search "copilot" and ensure it's enabled

## 5. 🔥 Clear Cache (If Still Not Working)

```
1. Press Ctrl+Shift+P (Cmd+Shift+P on Mac)
2. Type: "Developer: Reload Window"
3. Wait for VS Code to reload
4. Try signing in again
```

## 6. 🌐 Network Issues (For Corporate Networks)

If you're behind a firewall or proxy, you may need to:

- [ ] Configure proxy settings in VS Code
- [ ] Ask IT to whitelist these domains:
  - `github.com`
  - `api.github.com`
  - `copilot-proxy.githubusercontent.com`
  - `*.githubusercontent.com`

## 7. 📝 Test Copilot

After fixing:

1. Create a new file (e.g., `test.js`)
2. Type a comment: `// function to add two numbers`
3. Press Enter
4. You should see gray Copilot suggestions
5. Press Tab to accept

## Still Not Working?

See the full [Copilot Setup Guide](COPILOT_SETUP.md) for detailed troubleshooting steps.

---

**Most Common Solution**: Sign out of GitHub Copilot, restart VS Code, then sign in again. This fixes 90% of connection issues!
