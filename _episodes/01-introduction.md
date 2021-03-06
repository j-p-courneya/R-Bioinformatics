---
# Please do not edit this file directly; it is auto generated.
# Instead, please edit 01-introduction.md in _episodes_rmd/
title: "Introducing R and RStudio IDE"
teaching: 30
exercises: 15
questions:
- "Why use R?"
- "Why use RStudio and how does it differ from R?"
objectives:
- "Know advantages of analyzing data in R"
- "Know advantages of using RStudio"
- "Create an RStudio project, and know the benefits of working within a
   project"
- "Be able to customize the RStudio layout"
- "Be able to locate and change the current working directory with `getwd()` and
  `setwd()`"
- "Compose an R script file containing comments and commands"
- "Understand what an R function is"
- "Locate help for an R function using `?`, `??`, and `args()`"

keypoints:
- "R is a powerful, popular open-source scripting language"
- "You can customize the layout of RStudio, and use the project feature to manage the files and packages used in your analysis"
- "RStudio allows you to run R in an easy-to-use interface and makes it easy to find help"
source: Rmd
---



## Getting ready to use R for the first time

In this lesson we will take you through the very first things you need to get R working.

## A Brief History of R

[R](https://en.wikipedia.org/wiki/R_(programming_language)) has been around
since 1995, and was created by Ross Ihaka and Robert Gentleman at the University of Auckland, New Zealand. R is based off the S programming language developed at Bell Labs and was developed to teach intro statistics. See this [slide deck](https://www.stat.auckland.ac.nz/~ihaka/downloads/Massey.pdf) by Ross Ihaka for more info on the subject.

## Advantages of using R

At more than 20 years old, R is fairly mature and [growing in popularity](https://www.tiobe.com/tiobe-index/r/). However, programming isn’t a popularity contest. Here are key advantages of analyzing data in R:

 - **R is [open source](https://en.wikipedia.org/wiki/Open-source_software)**.
   This means R is free - an advantage if you are at an institution where you have to pay for your own MATLAB or SAS license. Open source, is important to your colleagues in parts of the world where expensive software is inaccessible. Being open source it also means that R is actively developed by a community (see [r-project.org](https://www.r-project.org/)), and there are regular updates.
 
 - **R is widely used**. Ok, maybe programming is a popularity contest.         Because, R is used in many areas (not just bioinformatics), you are more likely to find help online when you need it. Chances are, almost any error message you run into, someone else has already experienced.

- **R is powerful**. R runs on multiple platforms (Windows/MacOS/Linux). It can work with much larger datasets than popular spreadsheet programs like Microsoft Excel, and because of its scripting capabilities is far more reproducible. Also, there are thousands of available software packages for science, including genomics and other areas of life science.

> ## Discussion: Your experience
>
> What has motivated you to learn R? Have you had a research question for which spreadsheet programs such as Excel have proven difficult to use, or where the size of the data set created issues?
{: .discussion}


## Introducing RStudio

In these lessons, we will be making use of a software called [RStudio](https://www.rstudio.com/products/RStudio/),
an [Integrated Development Environment (IDE)](https://en.wikipedia.org/wiki/Integrated_development_environment).
RStudio, like most IDEs, provides a graphical interface to R, making it more
user-friendly, and providing dozens of useful features. We will introduce
additional benefits of using RStudio as you cover the lessons. 

>## What about this R app should I use that?
>
>Depending on what operating system youre using you will notice in your programs or application menu that there is R Studio and another software that is also R. Currently application icons look like this: 
>
><img src="../fig/notRuseRstudio.png" alt="r_and_rstudio_icons" style="width: 600px;"/>
>
>In case you end up launching R and not R Studio you will see an application window that looks like this: 
>
><img src="../fig/Rconsole.png" alt="r_console" style="width: 600px;"/>
>
>Go ahead and close it out. While there is nothing inherently wrong with using this. The features and benefits RStudio provides for programming in R significantly outweigh those of using the R console. Its recommended that you use RStudio. 
{: .callout}

## Overview and customization of the RStudio layout

Here are the major windows (or panes) of the RStudio
environment:

<img src="../fig/rstudio_session_4pane_layout.png" alt="rstudio default session" style="width: 1000px;"/>

- **Source**: This pane is where you will write/view R scripts. Some outputs
  (such as if you view a dataset using `View()`) will appear as a tab here.
- **Console/Terminal/Jobs**: This is actually where you see the execution of
  commands. This is the same display you would see if you were using R at the
  command line without RStudio. You can work interactively (i.e. enter R
  commands here), but for the most part we will run a script (or lines in a
  script) in the source pane and watch their execution and output here. The
  "Terminal" tab give you access to the BASH terminal (the Linux operating
  system, unrelated to R). RStudio also allows you to run jobs (analyses) in the background. This is useful if some analysis will take a while to run. You can see the status of those jobs in the background.
- **Environment/History**: Here, RStudio will show you what datasets and
  objects (variables) you have created and which are defined in memory.
  You can also see some properties of objects/datasets such as their type
  and dimensions. The "History" tab contains a history of the R commands you've executed R.
- **Files/Plots/Packages/Help/Viewer**: This multipurpose pane will show you the
  contents of directories on your computer. You can also use the "Files" tab to
  navigate and set the working directory. The "Plots" tab will show the output
  of any plots generated. In "Packages" you will see what packages are actively
  loaded, or you can attach installed packages. "Help" will display help files
  for R functions and packages. "Viewer" will allow you to view local web
  content (e.g. HTML outputs). 

All of the panes in RStudio have configuration options. For example, you can
minimize/maximize a pane, or by moving your mouse in the space between
panes you can resize as needed. The most important customization options for
pane layout are in the <KBD>View</KBD> menu. Other options such as font sizes,
colors/themes, and more are in the <KBD>Tools</KBD> menu under
<KBD>Global Options</KBD>.

>## You are working with R
> Although we won't be working with R at the terminal, there are lots of reasons to. For example, once you have written an RScript, you can run it at any Linux or Windows terminal without the need to start up RStudio. We don't want you to get confused - RStudio runs R, but R is not RStudio. For more on running an R Script at the terminal see this [Software Carpentry lesson](https://swcarpentry.github.io/r-novice-inflammation/05-cmdline/).
{: .callout}

## Create an RStudio project

One of the first benefits we will take advantage of in RStudio is something
called an **RStudio Project**. An RStudio project allows you to more easily:

- Save data, files, variables, packages, etc. related to a specific
  analysis project
- Restart work where you left off
- Collaborate, especially if you are using version control such as [git](http://swcarpentry.github.io/git-novice/).


1. To create a project, go to the <kbd>File</kbd> menu, and click <kbd>New Project...</kbd>.

2. In the window that opens select **New Directory**, then **New Project**. For "Directory name:" enter **post-docs_genomics_r**. For "Create project as subdirectory of", click <kbd>Browse...</kbd> and then click <kbd>Choose</kbd> which will select your `Documents` or `Desktop` directory.

3. Finally click <kbd>Create Project</kbd>. In the "Files" tab of your output
pane (more about the RStudio layout in a moment), you should see an RStudio
 project file, **post-docs_genomics_r.Rproj**. All RStudio projects end with the
 "**.Rproj**" file extension.
 
 Now when we start R in this project directory, or open this project with RStudio,
all of our work on this project will be entirely self-contained in this directory.

## Best practices for project organization

Although there is no "best" way to lay out a project, there are some general
principles to adhere to that will make project management easier:

### Treat data as read only

This is probably the most important goal of setting up a project. Data is
typically time consuming and/or expensive to collect. Working with them
interactively (e.g., in Excel) where they can be modified means you are never sure of where the data came from, or how it has been modified since collection.
It is therefore a good idea to treat your data as "read-only".

### Data Cleaning

In many cases your data will be "dirty": it will need significant preprocessing
to get into a format R (or any other programming language) will find useful. This
task is sometimes called "data munging". I find it useful to store these scripts
in a separate folder, and create a second "read-only" data folder to hold the
"cleaned" data sets.

### Treat generated output as disposable

Anything generated by your scripts should be treated as disposable: it should
all be able to be regenerated from your scripts.

There are lots of different ways to manage this output. I find it useful to
have an output folder with different sub-directories for each separate
analysis. This makes it easier later, as many of my analyses are exploratory
and don't end up being used in the final project, and some of the analyses
get shared between projects.

> ## Tip: Good Enough Practices for Scientific Computing
>
> [Good Enough Practices for Scientific Computing](https://github.com/swcarpentry/good-enough-practices-in-scientific-computing/blob/gh-pages/good-enough-practices-for-scientific-computing.pdf) gives the following recommendations for project organization:
>
> 1. Put each project in its own directory, which is named after the project.
> 2. Put text documents associated with the project in the `doc` directory.
> 3. Put raw data and metadata in the `data` directory, and files generated during cleanup and analysis in a `results` directory.
> 4. Put source for the project's scripts and programs in the `src` directory, and programs brought in from elsewhere or compiled locally in the `bin` directory.
> 5. Name all files to reflect their content or function.
>
{: .callout}

Now that you have been presented some practices to keep your data projects in R organized lets put the practice in to action. 

>## Exercise: Create sub-directories for your project.
>
>A) Create a `doc` directory to store text documents.
>
>B) Create a `data` directory for raw data and metadata
>
>C) Create a `results` directory for files generated during cleanup and analysis
>
>D) Create a `src` directory for your scripts.
>
>> ## Solution
>>
>>A) Using the RStudio <KBD>Files</KBD> tab in `pane 4` click the <KBD>New Folder</KBD> button. We will call the folder: `doc`
>>
>>B) Using the RStudio <KBD>Files</KBD> tab in `pane 4` click the <KBD>New Folder</KBD> button. We will call the folder: `data`
>>
>>C) Using the RStudio <KBD>Files</KBD> tab in `pane 4` click the <KBD>New Folder</KBD> button. We will call the folder: `results`
>>
>>D) Using the RStudio <KBD>Files</KBD> tab in `pane 4` click the <KBD>New Folder</KBD> button. We will call the folder: `src`
> {: .solution}
{: .challenge}

### Save some data in the data directory

Now we have a good directory structure we will now place/save data files in the `data/` directory.

> ## Challenge 1
> Download the `combined_tidy_vcf` data from  [here](https://osf.io/a325n/download).
>
> 1. Download the file 
> 2. Make sure it's saved under the name `combined_tidy_vcf.csv`
> 3. Save the file in the `data/` folder within your project.
>
> We will load and inspect these data later.
{: .challenge}

## Creating your first R script

Now that we are ready to start exploring R, we will want to keep a record of the
commands we are using. To do this we can create an R script:

Click the <kbd>File</kbd> menu and select <kbd>New File</kbd> and then
<kbd>R Script</kbd>. Before we go any further, save your script by clicking the
save/disk icon that is in the bar above the first line in the script editor, or
click the <kbd>File</kbd> menu and select <kbd>save</kbd>. In the "Save File"
window that opens, name your file **"genomics_r_basics"**. The new script
**genomics_r_basics.R** should appear under "files" in the output pane. By
convention, R scripts end with the file extension **.R**.

## Getting to work with R: navigating directories
Now that we have covered the more aesthetic aspects of RStudio, we can get to
work using some commands. We will write, execute, and save the commands we
learn in our **genomics_r_basics.R** script that is loaded in the Source pane.
First, lets see what directory we are in. To do so, type the following command into the script:


~~~
getwd()
~~~
{: .language-r}

To execute this command, make sure your cursor is on the same line the command
is written. Then click the <KBD>Run</KBD> button that is just above the first
line of your script in the header of the Source pane.


In the console, we expect to see the following output:

~~~
[1] "~/Documents/post-docs_genomics_r"
~~~
{: .output}

\* Notice, at the Console, you will also see the instruction you executed
above the output in blue.

Since we will be learning several commands, we may already want to keep some
short notes in our script to explain the purpose of the command. Entering a `#` , or using the keyboard short cut <KBD>Cntrl</KBD> + <KBD>Shift</KBD> + <KBD>C</KBD>, before any line in an R script turns that line into a comment, which R will not try to interpret as code. Edit your script to include a comment on the purpose of commands you are learning, e.g.:


~~~
# this command shows the current working directory
getwd()
~~~
{: .language-r}

> ## Exercise: Work interactively in R
>
> What happens when you try to enter the `getwd()` command in the Console pane?
>
>> ## Solution
>> You will get the same output you did as when you ran `getwd()` from the source. You can run any command in the Console, however, executing it from the source script will make it easier for us to record what we have done, and ultimately run an entire script, instead of entering commands one-by-one.
> {: .solution}
{: .challenge}

Next, lets create a folder in `Documents` or `Desktop` using the RStudio <KBD>Files</KBD> tab in `pane 4` using the <KBD>New Folder</KBD> button. We will call the folder: `R_data`. 

For the purposes of this exercise we want you to be in the directory `"~/Documents/R_data"`. What if you weren't? You can set your working directory using the `setwd()` command. Enter this command in your script, but *don't run* this yet.


~~~
# This sets the working directory
setwd()
~~~
{: .language-r}

You may have guessed, you need to tell the `setwd()` command
what directory you want to set as your working directory. To do so, inside of the parentheses, open a set of quotes. Inside the quotes enter a `~/` which is the home directory for Linux, Mac and Windows. Next, use the <KBD>Tab</KBD> key, to take advantage of RStudio's Tab-autocompletion method, to select `Documents` or `Desktop` depending on what you designated,
and the new folder `R_data` you just created. The path in your script should look like this:


~~~
# This sets the working directory
setwd("~/Documents/R_data")
~~~
{: .language-r}

When you run this command, the console repeats the command, but gives you no
output. Instead, you see the blank R prompt: `>`. Congratulations! Although it
seems small, knowing what your working directory is and being able to set your
working directory is the first step to analyzing your data.

> ## Tip: Never use `setwd()`
>
> Wait, what was the last 2 minutes about? Well, setting your working directory
> is something you need to do, you need to be very careful about using this as
> a step in your script. For example, what if your script is being on a computer
> that has a different directory structure? The top-level path in a Unix file
> system is root `/`, but on Windows it is likely `C:\`. This is one of several
> ways you might cause a script to break because a file path is configured
> differently than your script anticipates. R packages like [here](https://cran.r-project.org/package=here)
> and [file.path](https://www.rdocumentation.org/packages/base/versions/3.4.3/topics/file.path)
> allow you to specify file paths is a way that is more operating system
> independent. See Jenny Bryan's [blog post](https://www.tidyverse.org/articles/2017/12/workflow-vs-script/) for this
> and other R tips.
{: .callout}

>## Exercise
>
>Use `setwd()` to set the working directory back to the project directory you created in the "Create and RStudio Project" section. 
>
>> ## Solution
>> In your script write `setwd("~/Documents/post-docs_genomics_r")` or `setwd("~/Desktop/post-docs_genomics_r")` and hit <KBD>Control</KBD> + <KBD>Enter</KBD>. You can also write that in the console. Notice that you need to provide an absolute path to the directory/folder you are going to set the working directory to. 
>>
>> Alternatively you can use the <KBD>Files</KBD> tab in `pane 4` to navigate to your project folder, when there click the <KBD>More/Gear Icon</KBD> then select `Set as Working Directory`
> {: .solution}
{: .challenge}

## Using functions in R, without needing to master them

A function in R (or any computing language) is a short
program that takes some input and returns some output. Functions may seem like an advanced topic (and they are), but you have already
used at least one function in R. `getwd()` is a function! The next sections will help you understand what is happening in
any R script.

> ## Exercise: What do these functions do?
>
> Try the following functions by writing them in your script. See if you can
> guess what they do, and make sure to add comments to your script about your
> assumed purpose.
> - `dir()`
> - `sessionInfo()`
> - `date()`
> - `Sys.time()`
>
>> ## Solution
>> - `dir()` # Lists files in the working directory
>> - `sessionInfo()` # Gives the version of R and additional info including on attached packages
>> - `date()` # Gives the current date
>> - `Sys.time()` # Gives the current time
>>
>> *Notice*: Commands are case sensitive!
> {: .solution}
{: .challenge}

You have hopefully noticed a pattern - an R
function has three key properties:
- Functions have a name (e.g. `dir`, `getwd`); note that functions are case
  sensitive!
- Following the name, functions have a pair of `()`
- Inside the parentheses, a function may take 0 or more arguments

An argument may be a specific input for your function and/or may modify the
function's behavior. For example the function `round()` will round a number
with a decimal:


~~~
# This will round a number to the nearest integer
round(3.14)
~~~
{: .language-r}



~~~
[1] 3
~~~
{: .output}

## Getting help with function arguments

What if you wanted to round to one significant digit? `round()` can
do this, but you may first need to read the help to find out how. To see the help
(In R sometimes also called a "vignette") enter a `?` in front of the function
name:


~~~
?round()
~~~
{: .language-r}

The <KBD>Help</KBD> tab in `pane 4` will show you information (often, too much information). You
will slowly learn how to read and make sense of help files. Checking the "Usage" or "Examples"
headings is often a good place to look first. If you look under "Arguments," we
also see what arguments we can pass to this function to modify its behavior.
You can also see a function's argument using the `args()` function:


~~~
args(round)
~~~
{: .language-r}



~~~
function (x, digits = 0) 
NULL
~~~
{: .output}

`round()` takes two arguments, `x`, which is the number to be
rounded, and a
`digits` argument. The `=` sign indicates that a default (in this case 0) is
already set. Since `x` is not set, `round()` requires we provide it, in contrast
to `digits` where R will use the default value 0 unless you explicitly provide
a different value. We can explicitly set the digits parameter when we call the
function:


~~~
round(3.14159, digits = 2)
~~~
{: .language-r}



~~~
[1] 3.14
~~~
{: .output}

Or, R accepts what we call "positional arguments", if you pass a function
arguments separated by commas, R assumes that they are in the order you saw
when we used `args()`. In the case below that means that `x` is 3.14159 and
digits is 2.


~~~
round(3.14159, 2)
~~~
{: .language-r}



~~~
[1] 3.14
~~~
{: .output}

Finally, what if you are using `?` to get help for a function in a package not installed on your system, such as when you are running a script which has dependencies.


~~~
?geom_point()
~~~
{: .language-r}

will return an error:

~~~
Error in .helpForCall(topicExpr, parent.frame()) :
   no methods for ‘geom_point’ and no documentation for it as a function
~~~
{: .error}

Use two question marks (i.e. `??geom_point()`) and R will return
results from a search of the documentation for packages you have installed on your computer
in the "Help" tab. Finally, if you think there
should be a function, for example a statistical test, but you aren't
sure what it is called in R, or what functions may be available, use
the `help.search()` function.

> ## Exercise: Searching for R functions
> Use `help.search()` to find R functions for the following statistical
> functions. Remember to put your search query in quotes inside the function's
> parentheses.
>
> - Chi-Squared test
> - Student-t test
> - mixed linear model
>
>> ## Solution
>>   While your search results may return several tests, we list a few you might
>>   find:
>> - Chi-Squared test: `stats::Chisquare`
>> - Student-t test: `stats::TDist`
>> - mixed linear model: `stats::lm.glm`
> {: .solution}
{: .challenge}


We will discuss more on where to look for the libraries and packages that contain functions you want to use. For now, be aware that two important ones are [CRAN](https://cran.r-project.org/) - the main repository for R, and [Bioconductor](http://bioconductor.org/) - a popular repository for bioinformatics-related R packages which we will learn more about later.

## RStudio contextual help

Here is one last bonus we will mention about RStudio. It's difficult to
remember all of the arguments and definitions associated with a given function.
When you start typing the name of a function and hit the <KBD>Tab</KBD> key,
RStudio will display functions and associated help:

<img src="../fig/studio_contexthelp1.png" alt="rstudio default session" style="width: 600px;"/>

Once you type a function, hitting the <KBD>Tab</KBD> inside the parentheses
will show you the function's arguments and provide additional help
for each of these arguments.

<img src="../fig/studio_contexthelp2.png" alt="rstudio default session" style="width: 600px;"/>

## When you have no idea where to begin

If you don't know what function or package you need to use
[CRAN Task Views](http://cran.at.r-project.org/web/views)
is a specially maintained list of packages grouped into
fields. This can be a good starting point.

## When your code doesn't work: seeking help from your peers

If you're having trouble using a function, 9 times out of 10,
the answers you are seeking have already been answered on
[Stack Overflow](http://stackoverflow.com/). You can search using
the `[r]` tag. You can also Google it which typically takes you to a Stack Overflow post. 

If you can't find the answer, there are a few useful functions to
help you ask a question from your peers:


~~~
?dput
~~~
{: .language-r}

Will dump the data you're working with into a format so that it can
be copy and pasted by anyone else into their R session.


~~~
sessionInfo()
~~~
{: .language-r}



~~~
R version 4.0.4 (2021-02-15)
Platform: x86_64-apple-darwin17.0 (64-bit)
Running under: macOS Big Sur 10.16

Matrix products: default
BLAS:   /Library/Frameworks/R.framework/Versions/4.0/Resources/lib/libRblas.dylib
LAPACK: /Library/Frameworks/R.framework/Versions/4.0/Resources/lib/libRlapack.dylib

locale:
[1] en_US.UTF-8/en_US.UTF-8/en_US.UTF-8/C/en_US.UTF-8/en_US.UTF-8

attached base packages:
[1] stats     graphics  grDevices utils     datasets  methods   base     

other attached packages:
[1] knitr_1.33

loaded via a namespace (and not attached):
[1] compiler_4.0.4 magrittr_2.0.1 tools_4.0.4    stringi_1.7.3  stringr_1.4.0 
[6] xfun_0.24      evaluate_0.14 
~~~
{: .output}

Will print out your current version of R, as well as any packages you
have loaded. This can be useful for others to help reproduce and debug
your issue.

## Other ports of call

* [Quick R](http://www.statmethods.net/)
* [RStudio cheat sheets](http://www.rstudio.com/resources/cheatsheets/)
* [Cookbook for R](http://www.cookbook-r.com/)
