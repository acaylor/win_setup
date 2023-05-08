# win_setup
Scripts to setup my windows systems

### Install Chocolatey

To get started, you need to install Chocolatey on your Windows system. I have a script in my setup_win repository that runs the following command to download the latest installation script from the maintainers of Chocolatey:

That script needs to be run in an administrative shell:

[ Win Key ] + [ x ] + [ a ]

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force;
[System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072;
iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
⚠️
This will temporarily bypass the default PowerShell execution policy and run the installation script from Chocolatey's website. 
`choco install git`

And now we are ready to clone the repository. 

```powershell
cd C:\
git clone https://github.com/acaylor/win_setup.git
```

You need to open an administrative PowerShell inside my repo and run the `my_choco_pkgs.ps1` script:

```powershell
.\my_choco_pkgs.ps1
```

#### desktop-pkgs.config
This script installs packages that are in the `desktop-pkgs.config` XML file.

#### laptop-pkgs.config
This script installs packages that are in the `laptop-pkgs.config` XML file.

`.\my_laptop_pkgs.ps1`