# Installing Git and Setting Up Accounts

Git is a Version Control System (VCS) that has gained a lot of traction among the programming community.
We will want to use version control to keep track of the files we write, and the changes we make to them.

## Account Creation

During the course we will show you how to use [GitHub](https://www.github.com) to host some of your work and do code related project management. You will need to set up an account:

* Please [register](https://github.com/join) for a [GitHub](https://github.com/) account
* When choosing a username we recommend not using a name that includes an employer or university in case you move later on
  * i.e. 'johnsmith' or 'johnsmith86' are OK, 'johnsmithTilburg' probably not
* Apply for the education discount by following [these instructions](gh-edu)
  * Don't worry, we won't do anything that costs money in this course, the benefit is you get some perks

## Windows Users

We installed Git when we added a Bash Terminal in the previous step.
Check everything worked by [verifying your installation](#verifying your install)

## Mac Users

### Installing Git

We will install Git using Homebrew. Enter the following lines of code into your terminal:

``` bash
$ brew install git
$ brew link --force git
```

Then close and reopen the terminal. Now [Verify your installation](#verifying your install)

!!! bug "Git autocomplete for Older Macs (pre-2018)"

    On older generation Macs the terminal doesn't have this autocompletion for Git by default. 
    Let's add it using our trusty friend Homebrew.

    Open a terminal and enter:

    ``` bash
    $ brew install bash-completion
    ```

    This installs 'bash completion' into a file `/usr/local/etc/bash_completion.d`.

    To make the autocompletion work, type the following into your terminal:

    ```bash
    $ echo "[ -f /usr/local/etc/bash_completion ] && . /usr/local/etc/bash_completion" >> ~/.bash_profile
    ```

    And restart your terminal session:

    ``` bash
    $ source ~/.bash_profile
    ```

    Now you can autocomplete by pressing `tab` twice after a command.
    Enter the following into you terminal and press `tab` twice (which we depict as `[tab] [tab]`) below:

    ``` bash
    $ git [tab] [tab]
    ```

    which will then show the following (we only display the first and last few entries...):

    ```bash
    $ git [tab] [tab]
    add            blame          cherry-pick    ...         
    push           repack         rm             ...
    ...
    remote         revert         show-branch    tag
    ```

## Linux Users

Git should be installed already for you.
To check if it is, enter the following in a terminal:

``` bash
$ git --version
```

If you get a bunch of numbers (ideally starting with 2.15) or higher - you are good to move on.

If not, install it by entering the following into the command line:

``` bash
$ sudo apt-get install git
```

Once complete, [verify your install](#verifying-your-install).

## Verifying your install

To verify your installation, type the following command in a terminal and press the return key:

```bash
$ git --version
```

You should get an output that looks like:

```bash
git version 2.18.0
```

Ensure that you have a version greater than `2.15.0` installed.

[gh-edu]: https://docs.github.com/en/education/explore-the-benefits-of-teaching-and-learning-with-github-education/apply-for-an-educator-or-researcher-discount