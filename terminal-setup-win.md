# How to setup a development environment on Windows

Critical Making Studio | Fall 2017

This tutorial walks through setting up a development environment on Windows 10 similar to what is found on MacOS or any other Unix system. This guide walks through installing Git, ConEmu, Setting up SSH, connecting to a Github repo, and installing Miniconda for managing python environments.

## Install Git and ConEmu

1.  Download and install [Git for Windows](http://git-scm.com/download/win) with:
    * [X] Use Git from the Windows Command Prompt
2.  Download and install [ConEmu Installer](http://www.fosshub.com/ConEmu.html) (stable) 64 bit version.

## Configure ConEmu

1.  Start ConEmu (press Win key, write ConEmu and hit enter), the fast configuration screen should
    appear on the first launch, just click on OK.
2.  Open Settings (Win+Alt+P) and set:
    *  Startup:
        +  [X] Specified named task: `{Bash::Git bash}`
    *  Startup/Environment:
        +  Copy these lines to the text box. Don't delete the text in the box:

            ```
            set LANG=en_GB.UTF-8
            set LC_ALL=en_GB.UTF-8
            ```
    *  Main:
        +  [X] Clear Type
    *  Main/Confirm:
        +  [_] Confirm creating new console/tab (Win+W, toolbar [+])
        +  [_] Confirm tab closing
    *  Main/Update:
        +  [X] Check on startup
        +  [X] Stable (or Preview)
3.  Restart ConEmu

## Setup SSH and connect to Github Repository

1. Open up ConEmu and type ``git``. You should see the git help file.
2. Generate SSH key, if you don’t have one yet:
    *  `ssh-keygen` _(copy&paste to terminal and hit enter)_
    *  Use default key file location.
    *  Enter some password to protect your SSH key! You’ll be prompted to enter this password after
       opening terminal, but just once per Windows session (i.e. only after Windows reboot).
3. Check for existing keys to verify your keys have been made.
    * ``ls -al ~/.ssh``
4. Add your SSH key to the ssh-agent
    * Ensure the agent is running by entering ``eval $(ssh-agent -s)``
    * Add you SSH private key to the ssh-agent. ``ssh-add ~/.ssh/id_rsa``
5. Add your SSH key to your Github account
    * ``clip < ~/.ssh/id_rsa.pub`` to copy the key to the clipboard.
    * Goto Github> Settings and click add SSH key.
    * Enter a Title such as your computer name.
    * Paste the key into the "Key" field.
    * Click Add SSH Key
6. Proceed to checkout a repository, make changes to the files, commit, and push to verify it works with your computer and Github account.

## Setup Miniconda, make an environment, and install mkdocs

1. Download Miniconda for Windows 64-bit from https://conda.io/miniconda.html. I chose Miniconda vs Anaconda to save space. Anaconda will install alot of packages that are not needed at this time.
2. Install to custom directory
    * C:\Miniconda3
    * I chose this because my default install location had a space in the path and the installer indicated that several python packages might not work if using a path like this.
3. Choose to add Miniconda to PATH
    * [X] Check the option to Add Miniconda to my PATH environment variable
4. If you forget to check add to PATH option, you can manually add it by doing the following:
    * Open Anaconda Prompt (Terminal installed by Miniconda) and get some info
    * Locate the python executable ``where python``
    * ``C:\Miniconda3\python.exe``
    Locate the conda executable ``where conda``
    * ``C:\Miniconda3\Scripts\conda.exe``
    * Open Windows terminal and set the PATH based on this info:
    * ``SETX PATH "%PATH%;C:\Miniconda3\Scripts;C:\Miniconda3"``
5. Open ConEmu and verify python and conda are found
    * ``python --version`` should return the installed python version
    * ``conda list`` should list out a handfull of packages installed
6. Configure an environment and install python. Follow the [Conda Manual](https://conda.io/docs/user-guide/tasks/index.html).
    * ``conda create --name myenv``
    * ``source activate myenv`` to enter the environment
    * ``conda list`` to view all the packages installed. It will be the bare minimum to start but you can add more.
7. To install mkdocs
    * ``conda install -c conda-forge mkdocs``

**References**

* [Conda Install](https://conda.io/docs/user-guide/install/index.html)
* [Install Python on Windows (Anaconda)](https://medium.com/@GalarnykMichael/install-python-on-windows-anaconda-c63c7c3d1444)
* [Conda Manual](https://conda.io/docs/user-guide/tasks/index.html)




