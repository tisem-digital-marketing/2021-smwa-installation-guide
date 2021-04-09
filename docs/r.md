# R

R is a language for statistical computing and graphics.
R's use in the data science and marketing analytics community has taken off over recent years and (at a bare minimum) should be considered as an open source replacement to software such as SAS, SPSS and Stata.

## Installing R Windows Users

Go to the [R homepage for Windows] and download the most recent installer (`R-4.0.5-win.exe`)

To install, double-click the `exe` you just downloaded and follow the instructions.

<!-- Once you have installed R, [verify your install](#verifying-your-install-of-r-all-users). -->

## Installing R for Mac Users

Go to the [R homepage](https://cran.r-project.org/) and download the installer (`R-4.0.5.pkg`).

To install, double-click the `pkg` and follow the instructions.

<!-- Once you have installed R, [verify your install](#verifying-your-install-of-r-all-users). -->

!!! tip "Why Not Install via Homebrew?"
        There is conflicting views on Homebrew's installation of `R`.
        Because we haven't tried it to ensure no problems will emerge, we recommend going with the installation based on the CRAN distributed package.

## Installing R for Linux

First, we need to import the signing key:

```bash
$ apt-key adv --keyserver keyserver.ubuntu.com --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9
```

add a repository so that our operating system knows where to install the most recent version of `R` from.

Enter the following into the terminal and press `Return`:

```bash
$ add-apt-repository "'deb https://cloud.r-project.org/bin/linux/ubuntu '$(lsb_release -sc)'-cran40/'"
```

where we use `lsb_release -cs` to access which Ubuntu flavor you run: one of “groovy”, “focal”, “bionic”, …

Now, update to get the package manifests from the new repository:

```bash
$ sudo apt-get update
```

We can now install `R` as from the terminal by entering the following:

```{bash}
$ sudo apt-get install r-base r-base-dev
```

Install the multi-threaded OpenBlas library to get higher performance for linear algebra operations:

```{bash}
$ sudo apt-get install libopenblas-base
```

<!-- Now, [verify your install](#verifying-your-install-of-r-all-users).

!!! warning "R on WSL Ubuntu vs. R on native Windows"
        Even if you already have a version of `R` installed on your Windows machine, you need to install `R` inside the WSL Ubuntu 18.04 environment we have set up.
        Your Ubuntu terminal cannot see everything you have on your native Windows installation. -->

<!-- ## Verifying your Install of R - All Users

Open a bash terminal and enter:

```bash
$ R --version
```

followed by pressing `Return`. The expected return begins with:

```bash
R version 4.0.x (2021-xx-xx) -- "Some Funky Name"
``` -->
