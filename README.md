# Windows 11 Setup with Chocolatey (for Python Developers and Data Scientists)

Easily configure your Windows 11 machine for an efficient workflow using Chocolatey and PowerShell (just like `sudo apt-get`).

## Installation Steps:

1. Install Chocolatey(run command in CMD as admin)
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "[System.Net.ServicePointManager]::SecurityProtocol = 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"

3. Download trusted packages using Chocolatey (there you can find other packages).
4. Install software from a local directory if desired.
5. Optionally, set up drivers for your laptop.
6. Use the `-a` flag to accept all installations.

These instructions have been tested on an MSI laptop with Windows 11 and various virtual machines.

### PowerShell Commands - RUN ONLY AS ADMIN

```powershell
Get-ExecutionPolicy
Set-ExecutionPolicy AllSigned

Set-ExecutionPolicy Bypass -Scope Process -Force;
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072;
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/inst...'))


choco install vim wsl2 sublimetext3.app cpu-znvidia-driver ccleaner dotnetfx zoom google-drive-file-stream jre8 vcredist140 totalcommander winrar flashplayerplugin notepad excel word powerbi adobereader npppluginmanager virtualbox vmware-workstation putty mobaxterm pycharm-community visualstudio visualstudio2019 vmim microsoft-windows-subsystem-linux git mongodb docker python miniconda nvim-ui vim ntop.portable wsl mysql postgresql dbeaver docker-engine docker-desktop lightshot telegram googlechrome whatsapp figma -y -A

```
### Additional Commands for Customization (you can modify for your own setup):

#### Install General Software
```
choco install totalcommander
choco install ccleaner
choco install winrar
choco install npppluginmanager
choco install powerbi
choco install adobereader
choco install flashplayerplugin
choco install jre8
choco install vcredist140
choco install zoom
choco install google-drive-file-stream
choco install dotnetfx
```
#### Install Tech Software
```separate packages
choco install python
choco install miniconda
choco install virtualbox
choco install vmwareworkstation
choco install putty
choco install mobaxterm
choco install pycharm
choco install vscode
choco install nvim-ui
choco install vim
choco install ntop.portable
choco install wsl
choco install git
choco install mysql
choco install postgresql
choco install mongodb
choco install dbeaver
choco install docker
choco install docker-engine
choco install docker-desktop
```

#### Install Social media
```
choco install googlechrome
choco install telegram
choco install figma
```
#### Install Design and presentation Software
```
choco install figma -y
choco install photoshop -y
choco install 3dsmax -y
```
