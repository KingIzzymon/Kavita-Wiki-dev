---
title: 'macOS'
---

### Introduction
! No one on the dev team owns a Mac. These instructions are suggested by our users. If you think you can improve them, please [submit a PR](https://github.com/Kareadita/Wiki/edit/main/pages/02.install/04.macos/default.md).

1. [Download Kavita for macOS](https://www.kavitareader.com/#downloads-v1-macos). The file you want is "kavita-osx-x64.tar.gz".

2. Unpack Kavita to your User Folder or folder of choice. For example, in Terminal:
    * `cd ~`
    * `mv ~/Downloads/kavita-osx-x64.tar.gz ~`
    * `tar -xf kavita-osx-x64.tar.gz`

3. Make Kavita executable.
    * `sudo chmod +x ~/Kavita/Kavita`

4. Disable Gatekeeper for Kavita's folder so that Kavita and all .dll and .dylib files can be opened
    * `xattr -r -d com.apple.quarantine ~/Kavita/`

5. Help Kavita find sqlite
    * `export alias sqlite=sqlite3`

6. Start Kavita in Terminal. You need to launch Kavita from within the `~/Kavita` folder, or else `appsettings.json` will fail to be acquired.
    * `cd ~/Kavita`
    * `./Kavita`

7. Open a browser window, at address: http://localhost:5000/

### Troubleshooting
1. If you see an error like the following, please edit the file `config/appsettings.json` and change the Port, e.g. `"Port": 5555`. 
    * <i>`Unhandled exception. System.IO.IOException: Failed to bind to address http://[::]:5000: address already in use.`</i>

2. Open a browser window, at the new address: http://localhost:5555/

