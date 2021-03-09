# Bash Shell

A command-line interface or shell, also known as a terminal, is a means of interacting with a computer program where the user issues commands to the program in the form of successive lines of text.

We will want to use the `Bash` shell for this course to interact with our file system and use Git.

## Windows Users

Windows doesn't have a Bash shell by default, so we are going to install one.
Follow these steps:

1. Download the Git for Windows [installer](https://gitforwindows.org/).
2. Run the installer and follow the steps below:
    * Click on "Next" four times (two times if you've previously installed Git). You don't need to change anything in the Information, location, components, and start menu screens.
    * From the dropdown menu select "Use the Nano editor by default" (NOTE: you will need to scroll up to find it) and click on "Next".
    * On the page that says "Adjusting the name of the initial branch in new repositories", ensure that "Let Git decide" is selected. This will ensure the highest level of compatibility for our lessons.
    * Ensure that "Git from the command line and also from 3rd-party software" is selected and click on "Next". (If you don't do this Git Bash will not work properly, requiring you to remove the Git Bash installation, re-run the installer and to select the "Git from the command line and also from 3rd-party software" option.)
    * Ensure that "Use the native Windows Secure Channel Library" is selected and click on "Next".
    * Ensure that "Checkout Windows-style, commit Unix-style line endings" is selected and click on "Next".
    * Ensure that "Use Windows' default console window" is selected and click on "Next".
    * Ensure that "Default (fast-forward or merge) is selected and click "Next"
    * Ensure that "Git Credential Manager Core" is selected and click on "Next".
    * Ensure that "Enable file system caching" is selected and click on "Next".
    * Click on "Install".
    * Click on "Finish" or "Next".
3. If your "HOME" environment variable is not set (or you don't know what this is):
    * Open command prompt (Open Start Menu then type cmd and press Enter)
    * Type the following line into the command prompt window exactly as shown:
      `setx HOME "%USERPROFILE%"`
    * Press Enter, you should see SUCCESS: Specified value was saved.
    * Quit command prompt by typing exit then pressing Enter

This will provide you with both a Bash (called GitBash) shell *and Git*.

To verify you have installed GitBash, click the windows button, and type in 'GitBash'.
You should see the software appear as a 'choice'.
Click on it, and a bash terminal should open up.

## Mac Users

A Bash shell comes already installed with MacOS.

You will need to install some other software from the terminal throughout the course, so it will be useful to install some additional "command line tools" now.

### Opening a Terminal Session

To open a terminal session:

* Open spotlight with `cmd + space`
* Type in 'terminal'
* When the terminal appears, open it.

### Installing New Tools for the Terminal

#### The X-code Tools

We want to install 'X-code command line tools'. Copy and paste the following and press `Return`

``` bash
xcode-select --install
```

If you get a message that the command line tools are already installed, you can continue to the next step.

#### Homebrew Package Manager

Homebrew is a package manager for Mac.

Install Homebrew by opening a terminal and pasting the following command:

``` bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Verify that Homebrew installed correctly, enter the following into your terminal:

``` bash
brew doctor
```

And you should see the following output:

``` bash
Your system is ready to brew
```

Before continuing, lets be sure everything in Homebrew is up to date by entering the following:

``` bash
brew upgrade
```

### Installing Packages with Homebrew

Now we can use homebrew to easily install software.  We need some basic system tools for some of the R packages we will install later.

In particular we need:

* `libxml2`
* `openssl`
* `libgit2`

Most of these are already installed, but we need updates of these packages.
For each of these packages enter:

``` bash
brew reinstall pkg-name
```

i.e. `brew reinstall libxml2`.

If you get a message that the package you are trying to reinstall is not yet installed, try `brew install pkg-name` instead.

### Linking Packages to a Terminal Session

We need to ensure that our terminal session has access to what we installed.
To do this, copy and paste the following into your bash shell:

``` bash
echo 'export PATH="/usr/local/opt/libxml2/bin:$PATH"' >> ~/.bash_profile
echo 'export PATH="/usr/local/opt/openssl/bin:$PATH"' >> ~/.bash_profile
source .bash_profile
```

## Linux Users

* Linux Users: Open a terminal session with `Ctrl` + `Alt` + `T`.
* Windows Users: Open the Ubuntu Terminal as we described [here](/windows-wsl/#installing-windows-terminal)

Copy the following command into terminal and press `Return`:

```bash
sudo apt-get update
sudo apt-get install libcurl4-gnutls-dev librtmp-dev
```

After the installation succeeded successfully repeat this one-by-one with the following two other commands:

```bash
sudo apt-get install libxml2-dev
sudo apt-get install libssl-dev
# below needed to install R
sudo apt install --no-install-recommends software-properties-common dirmngr 
```
