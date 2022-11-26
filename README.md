# windows11-Set-Up-Chocolatey
Makeing devlopment environment with chocolatry in windows11

## What is Chacolatey
Chocolatey is the package manager for windows like apt or brew.  
With setting up your Windows11 PC, you can easily manage packages like Linux.  
For more infomation see here -> https://chocolatey.org/


## Goals
+ Google Chrome
+ VSCode Editor
+ Git
+ NodeJS
+ Python with pyenv and poetry
+ WSL
+ Docker

## Install Chocolatey
Details are here -> https://chocolatey.org/install
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))```
3. Paste the copied text into your shell and press Enter.
4. Wait a few seconds for the command to complete.
5. If you don't see any errors, you are ready to use Chocolatey! Type choco or choco -? now, or see Getting Started for usage instructions.

## Google Chrome
Details here -> https://community.chocolatey.org/packages/GoogleChrome  
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```choco install googlechrome -y```
3. (Optional) Set Default Browser to Chrome  
Looking here -> https://www.itechguides.com/how-to-change-default-browser-in-windows-11/

## VSCode
Details here -> https://community.chocolatey.org/packages/vscode  
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```choco install vscode -y``` or ```code --version```
3. Exit your powershell, and reopen powershell or cmd
4. Check your vscode works fine(Copy and Paste)  
```code .```

## Git
Details here -> https://community.chocolatey.org/packages/git  
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```choco install git -y```
3. Exit your powershell, and reopen powershell or cmd
4. Check your git works fine(Copy and Paste)  
```git --version```

## Node.js(LTS)
Details here -> https://community.chocolatey.org/packages/git  
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```choco install nodejs-lts -y```
3. Exit your powershell, and reopen powershell or cmd
4. Check your git works fine(Copy and Paste)  
```node --version``` and ```npm --version``` and ```npx --version```
