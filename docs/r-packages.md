# Additional R Packages

We will need some additional libraries to conduct our statistical analysis.
The packages we install here will be the main packages for the class.

We may ask you to install other packages as the course progresses.

## All Users

Proceed as follows:

* Open RStudio
* In the **console**, copy and paste the following:

```r
to_install <-c( "tidyverse",
                "tidymodels",
                "rmarkdown",
                "knitr",
                "fixest",
                "margins",
                "modelsummary",
                "renv",
                "tidytext",
                "textstem",
                "wordcloud",
                "reshape2",
                "textrecipes",
                "vip",
                "assertr",
                "haven"
                )

install.packages(to_install)
```

* If you are asked if you want to install packages that need compilation, type `y` followed by `Return` to confirm this.
* Wait until all the packages have been installed and the you are done.
  * It *may* take a while, so be patient
