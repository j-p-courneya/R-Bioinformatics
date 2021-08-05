---
title: Setup
---
## 1) Install R and RStudio

* Install [R, a free software environment for statistical computing and graphics][r-proj] from [CRAN][cran], the Comprehensive R Archive Network. We __highly recommend__ you install a precompiled binary distribution for your operating system -- use the links up at the top of the CRAN page linked above!

* Install RStudio's IDE (stands for _integrated development environment_), a powerful user interface for R. Get the Open Source Edition of RStudio Desktop.

  - It's __highly recommend__ you run the [Preview version][rstudio-preview]. We find these quite stable and you'll get the cool new features! Update to new Preview versions often.
  - Of course, there are also official releases available [here][rstudio-official].
  - RStudio comes with a __text editor__, so there is no immediate need to install a separate stand-alone editor.
  - RStudio can __interface with Git(Hub)__. However, you must do all the Git(Hub) set up before you can take advantage of this.
    
If you have a pre-existing installation of R and/or RStudio, we __highly recommend__ that you reinstall both and get as current as possible. It can be considerably harder to run old software than new.

* If you upgrade R, you will need to update any packages you have installed. The command below should get you started, though you may need to specify more arguments if, e.g., you have been using a non-default library for your packages.

    ``` r
    update.packages(ask = FALSE, checkBuilt = TRUE)
    ```

  __Note:__ this will only look for updates on CRAN. So if you use a package that lives *only* on GitHub or if you want a development version from GitHub, you will need to  update manually, e.g. via `devtools::install_github()`.

### Testing testing

* Do whatever is appropriate for your OS to launch RStudio. You should get a window similar to the screenshot you see [here][rstudio-workbench], but yours will be more boring because you haven't written any code or made any figures yet!

* Put your cursor in the pane labelled Console, which is where you interact with the live R process. Create a simple object with code like `x <- 2 * 4` (followed by enter or return). Then inspect the `x` object by typing `x` followed by enter or return. You should see the value 8 print to screen. If yes, you've succeeded in installing R and RStudio.

### Further resources

The above will get your basic setup ready but here are some links if you are interested in reading a bit further.

* [How to Use RStudio][rstudio-support]
* [RStudio's leads for learning R][rstudio-R-help]
* [R FAQ][cran-faq]
* [R Installation and Administration][cran-R-admin]
* [More about add-on packages in the R Installation and Administration Manual][cran-add-ons]

## Attributions

The preceding materials were greatly influenced and produced from existing materials found in [happygitwithR][happy-git]. Thank you to the happygitwithR team! 


{% include links.md %}
