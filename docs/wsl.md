# Setting up Windows Subsystem for Linux (WSL)
Prerequisites:
- Windows 10 with the Anniversary Update

## Installing Ubuntu
Open PowerShell as an Administrator and run the following command:
```
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

Go to the Microsoft store, and then search and install Ubuntu. Click "Launch" when the download is done and create your Linux user account from the popup console window. Remember your password! Your password will be needed when you need to run commands with elevated privileges (e.g. sudo).

You can now open Bash by running the Ubuntu app you previously installed. Although not required, changing the default colors is highly recommended. To do this, right click the top left Ubuntu icon and click on "Properties". Go to the "Colors" tab from the popup window and then change the colors to whatever you want, or just follow the instructions [here](https://medium.com/@jgarijogarde/make-bash-on-ubuntu-on-windows-10-look-like-the-ubuntu-terminal-f7566008c5c2) to get to the default Ubuntu terminal colors.

Test out some commands, e.g.:
```
$ ls -la
$ pwd
```

If you want to change your starting directory when you open Bash, edit your ~.bashrc file with your editor of choice. To do this with vim, first open the ~.bash.rc file with vim:
```
$ cd ~
$ vim .bashrc
```

Press "i" to go into insert mode, then add the following line at the top:
```
cd DIRECTORY_THAT_I_WANT_TO_START_ON
```

An example of a typical directory would be ```/mnt/c/Users/My_Username/Documents/Projects```. Get out of insert mode by pressing escape, and then entering in ```wq``` and press Enter.

Here are some command line resources if you want to learn more: [The Linux Command Line](http://www.linuxzasve.com/preuzimanje/TLCL-09.12.pdf), [A-Z index of Bash commands](https://ss64.com/bash/)

## Setting up Python
Update your package list by running:
```
$ sudo apt-get update
```

Then install Python 3 and pip:
```
$ sudo apt-get install python3
$ sudo apt-get install python-pip
```

Install virtualenv with pip:
```
$ pip install virtualenv
```

Remember to work in virtual environments for your projects!

## Setting up Node.js
Install Node.js 9:
```
$ curl -sL https://deb.nodesource.com/setup_9.x | sudo -E bash - sudo apt-get install -y nodejs
```

To compile and install native addons from npm you may also need to install build tools:
```
$ sudo apt-get install -y build-essential
```
