# windows11-Set-Up-Chocolatey
Makeing devlopment environment with chocolatry in windows11  
This tutorial is for datascientists mainly

## What is Chocolatey
Chocolatey is the package manager for windows like apt or brew.  
With setting up your Windows11 PC, you can easily manage packages like Linux.  
For more infomation see here -> https://chocolatey.org/


## Goals
- For everyone
  - Google Chrome
- For every developers
  - VSCode
  - Git
  - WSL + Docker
- For js/ts engineers
  - Node.js
- For python engineers
  - Python(pyenv + poetry)
  - Anaconda


## Install Chocolatey
Details are here -> https://chocolatey.org/install
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
3. Paste the copied text into your shell and press Enter.
4. Wait a few seconds for the command to complete.
5. If you don't see any errors, you are ready to use Chocolatey! Type choco or choco -? now, or see Getting Started for usage instructions.

## Google Chrome
Details here -> https://community.chocolatey.org/packages/GoogleChrome  
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```
choco install googlechrome -y
```
3. (Optional) Set Default Browser to Chrome  
Looking here -> https://www.itechguides.com/how-to-change-default-browser-in-windows-11/

## VSCode
Details here -> https://community.chocolatey.org/packages/vscode  
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```
choco install vscode -y
``` 
3. Exit your powershell, and reopen powershell or cmd
4. Check your vscode works fine(Copy and Paste)  
```
code --version
```
or
```
code .
```


## Git
Details here -> https://community.chocolatey.org/packages/git  
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```
choco install git -y
```
3. Exit your powershell, and reopen powershell or cmd
4. Check your git works fine(Copy and Paste)  
```
git --version
```

## WSL + Docker
### WSL part(Not using chocolatey)
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```
wsl --install
```
3. Rstart Computer(Copy and Paste)  
```
Restart-Computer
```
4. When your PC restarts, ubuntu shell will open automatically. Enter username and password.
5. Exit Ubuntu shell
6. Open powershell or cmd, and check wsl works fine.
```
wsl --version
```
or
```
wsl
```

### Docker part
Details here -> https://community.chocolatey.org/packages/docker-desktop, https://community.chocolatey.org/packages/docker-compose  
1. First, ensure that you are using an administrative "cmd shell" - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```
choco install docker desktop -y
```
3. Refresh Environment Variables on the cmd
```
refreshenv
```
4. Check docker works fine
```
docker --version
```
5. Install docker-compose
```
choco install docker-compose -y
```
6. check docker-compose works fine
```
docker-compose --version
```

## Node.js(LTS)
Details here -> https://community.chocolatey.org/packages/nodejs-lts  
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.  
2. Install with powershell.exe(Copy and Paste)  
```
choco install nodejs-lts -y
```
3. Exit your powershell, and reopen powershell or cmd
4. Check your node and npm works fine(Copy and Paste)  
```
node --version
```
and
```
npm --version
```
and
```
npx --version
```

## Python(pyenv + poetry)
### pyenv part
Details here -> https://community.chocolatey.org/packages/pyenv-win  
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```
choco install pyenv-win -y
```
3. Change app alias
   - Right click on the windows mark and open settings (```win + i``` is also open settings)
   - Click Apps and choose Advanced app settings
   - Click execution aliases
   - Trun off both "App installer" python.exe and python3.exe
4. Open Environment variables and Open Path in "User Valiables"
   - When you open User Path variables, maybe looks like Before.
     ```
     Before 
 
     %USERPROFILE%\AppData\Local\Microsoft\WindowsApps
     ...
     ...
     ...
     %USERPROFILE%\.pyenv\pyenv-win\bin
     %USERPROFILE%\.pyenv\pyenv-win\shims
     ```
   - Change the order to After
     ```
     After

     %USERPROFILE%\.pyenv\pyenv-win\bin
     %USERPROFILE%\.pyenv\pyenv-win\shims
     ...
     ...
     ...
     %USERPROFILE%\AppData\Local\Microsoft\WindowsApps
     ```
    
   - Click Ok and close Environment Variables
5. Exit your powershell, and reopen cmd (not powershell!!)
6. Check your pyenv works fine(Copy and Paste)  
```
pyenv --version
```
7. Check python versions you can choose  
```
pyenv install --list
```
8. Deside python version you need
9. Install Python you want (I installed 3.10.5 and 3.9.13)
```
pyenv install 3.10.5
pyenv install 3.9.13
```
12. Check the versions of python you installed  
```
pyenv versions
```
13. Set python version use globaly or current folda
    - On globaly use  
      ```pyenv global 3.10.5 ```
    - On current folda use (If you set local, local version has priority on the folda)  
     ```pyenv local 3.9.13```
14. Check current python version works fine  
```
pyenv version
```

### poetry part(Not using chocolatey)
Details here -> https://python-poetry.org/docs/  
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```
(Invoke-WebRequest -Uri https://install.python-poetry.org -UseBasicParsing).Content | python -
```
3. Open Environment variables and Open Path in "User Valiables"
   - When you open User Path variables, maybe looks like Before.
     ```
     Before

     %USERPROFILE%\.pyenv\pyenv-win\bin
     %USERPROFILE%\.pyenv\pyenv-win\shims
     ...
     ...
     ...
     %USERPROFILE%\AppData\Local\Microsoft\WindowsApps
     ```
   - Change the order to After
     ```
     After

     %USERPROFILE%\.pyenv\pyenv-win\bin
     %USERPROFILE%\.pyenv\pyenv-win\shims
     %APPDATA%\Python\Scripts
     ...
     ...
     ...
     %USERPROFILE%\AppData\Local\Microsoft\WindowsApps
     ```
4. Reopen administrative shell
5. Check poetry works fine
```
poetry --version
```

##Anaconda
Details here -> https://community.chocolatey.org/packages/git  
1. First, ensure that you are using an administrative shell - you can also install as a non-admin, check out Non-Administrative Installation.
2. Install with powershell.exe(Copy and Paste)  
```
choco install anaconda3 -y
```
4. Open Environment variables and Open Path in "System variables"
5. Add Paths at bottom like this
   ```
   ...
   ...
   ...
   C:\tools\Anaconda3\Library
   C:\tools\Anaconda3\Library\mingw-w64
   C:\tools\Anaconda3\Library\usr\bin
   C:\tools\Anaconda3\Library\bin
   C:\tools\Anaconda3\Scripts
   ```
6. Exit your shell, and reopen powershell or cmd
7. Check conda works fine
```
conda --version
```
