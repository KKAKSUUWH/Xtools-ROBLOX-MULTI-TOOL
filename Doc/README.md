# Roblox Account Generator Setup Guide

## 🖥️ System Requirements
- **Windows 10/11** (64-bit)
- **Node.js 16+** [Download](https://nodejs.org/)
- **Dedicated folder** for the application files

## 🛠️ Installation & Setup
1. **Create Application Folder**
   ```bash
   mkdir Xtools
   cd Xtools
   ```
2. **Install Prerequisites**
   - Install Node.js using default settings

3. **Application Setup**
   - Place these files in your folder:
     - `XtoolsV1.1.exe`
     - `input/config.json`
     - `input/proxies.txt`
   - Folder structure should look like:
     ```
     Xtools/
     ├── XtoolsV1.1.exe
     └── Config/
         └── XtoolsConfig.json
     ```

## 🔑 Initial Configuration
1. **Claim Your License Key**
   - In our Discord server, type: `/claim YOUR_LICENSE`
   - You'll claim your key

2. **Configure XtoolsConfig.json**
   ```json
   {
       "LicenseKey": "YOUR_LICENSE",
   }
   ```

## 🚨 Common Issues & Solutions

### ❌ Program Closes Immediately
**Fix:**
1. Right-click `XtoolsV1.1.exe` > "Run as administrator"
2. Verify folder structure matches requirements
3. Ensure you claimed and added and saved the config json
4. Ensure you are not running any reverse engineering software
5. Hwid matches the hwid used before
6. Disable antivirus/firewall if experiencing false positives

### ❌ "Invalid Hardware ID" Error
**Resolution:**
```bash
# In Discord:
/request-hwid-reset
```
Contact @Admin in Discord if issues persist


## 🔄 HWID Management
- Keys are permanently bound to your hardware
- For hardware changes:
  ```bash
  # Discord command:
  /request-hwid-reset
  ```
- Admins will process reset requests within 24 hours


## 📌 Important Notes
- Never share your `XtoolsConfig.json` file or license key
- Keep application files in their original folder
- Disable antivirus/firewall if experiencing false positives

## 🆘 Support
Create a ticket in our Discord Server with:
1. Error screenshot
2. `config.json` (redact your rosolve key)
3. System specs

[![Join Discord](https://img.shields.io/badge/Join%20Us%20on%20Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discord.gg/ajgUhUHEmG)