# GitHub Copilot Setup and Troubleshooting Guide

This guide will help you resolve common GitHub Copilot connection and login issues in VS Code.

## Prerequisites

1. **GitHub Copilot Subscription**: Ensure you have an active GitHub Copilot subscription
   - Individual subscription or
   - Access through your organization/enterprise

2. **VS Code Version**: Use the latest version of Visual Studio Code
   - Download from: https://code.visualstudio.com/

## Installation Steps

### 1. Install GitHub Copilot Extension

1. Open VS Code
2. Click on Extensions icon (or press `Ctrl+Shift+X` / `Cmd+Shift+X`)
3. Search for "GitHub Copilot"
4. Install both:
   - **GitHub Copilot** (by GitHub)
   - **GitHub Copilot Chat** (by GitHub)

### 2. Sign in to GitHub

1. After installing the extensions, you'll see a notification to sign in
2. Click **Sign in to GitHub**
3. You'll be redirected to your browser
4. Authorize the GitHub Copilot extension
5. Return to VS Code

## Troubleshooting Common Issues

### Issue 1: Cannot Sign In / Login Fails

**Solution A: Clear VS Code Authentication Cache**

1. Open Command Palette (`Ctrl+Shift+P` / `Cmd+Shift+P`)
2. Type and select: `Developer: Reload Window`
3. Try signing in again

**Solution B: Sign Out and Sign In Again**

1. Open Command Palette
2. Type: `GitHub Copilot: Sign Out`
3. Restart VS Code
4. Open Command Palette
5. Type: `GitHub Copilot: Sign In`

**Solution C: Check GitHub Authentication**

1. Open Command Palette
2. Type: `Accounts: Sign Out of GitHub`
3. Type: `Accounts: Sign In to GitHub`
4. Complete the browser authentication flow

### Issue 2: Copilot Not Connecting

**Check Extension Status:**

1. Look at the bottom-right corner of VS Code
2. Check the Copilot icon status
3. If it shows an error, click on it for details

**Enable Copilot:**

1. Open Command Palette
2. Type: `GitHub Copilot: Enable`
3. Or click the Copilot icon in the status bar

### Issue 3: Firewall/Proxy Issues

If you're behind a corporate firewall or proxy:

1. Configure VS Code proxy settings in `settings.json`:
   ```json
   {
     "http.proxy": "http://your-proxy:port",
     "http.proxyStrictSSL": false
   }
   ```

2. Ensure these domains are whitelisted:
   - `github.com`
   - `api.github.com`
   - `copilot-proxy.githubusercontent.com`
   - `*.githubusercontent.com`

### Issue 4: Suggestions Not Appearing

1. Verify inline suggestions are enabled:
   - Open Settings (`Ctrl+,` / `Cmd+,`)
   - Search for "inline suggest"
   - Ensure **Editor: Inline Suggest Enabled** is checked

2. Check Copilot settings:
   - Open Command Palette
   - Type: `Preferences: Open Settings (JSON)`
   - Verify these settings:
     ```json
     {
       "editor.inlineSuggest.enabled": true,
       "github.copilot.enable": {
         "*": true
       }
     }
     ```

### Issue 5: Organization Access Issues

If you're part of an organization:

1. Check your organization's Copilot policy:
   - Go to https://github.com/settings/copilot
   - Verify your organization has enabled Copilot for you

2. Contact your organization administrator if needed

## Manual Configuration

This repository includes VS Code workspace settings that should automatically configure Copilot. If they don't apply:

1. Open the workspace in VS Code
2. When prompted, install recommended extensions
3. Reload the window if necessary

## Verifying Installation

1. Open any code file (e.g., create a new `.js` or `.py` file)
2. Start typing a comment or function
3. You should see gray suggestions from Copilot
4. Press `Tab` to accept suggestions

## Getting Help

- **GitHub Copilot Documentation**: https://docs.github.com/en/copilot
- **VS Code Issues**: https://github.com/microsoft/vscode/issues
- **Copilot Extension Issues**: https://github.com/github/copilot.vim/issues

## Quick Commands Reference

- **Sign In**: `Ctrl+Shift+P` → `GitHub Copilot: Sign In`
- **Sign Out**: `Ctrl+Shift+P` → `GitHub Copilot: Sign Out`
- **Enable/Disable**: Click Copilot icon in status bar
- **Open Settings**: `Ctrl+,` (or `Cmd+,` on Mac)
- **Reload Window**: `Ctrl+Shift+P` → `Developer: Reload Window`

## Additional Tips

1. **Keep Extensions Updated**: Regularly update the Copilot extensions
2. **Restart VS Code**: Many issues are resolved by simply restarting VS Code
3. **Check GitHub Status**: Visit https://www.githubstatus.com/ to check for service outages
4. **Review Logs**: Open Output panel and select "GitHub Copilot" to view logs

## Contact

If you continue experiencing issues after following this guide, please open an issue in this repository with:
- Your VS Code version
- Your operating system
- Detailed description of the problem
- Any error messages you're seeing
