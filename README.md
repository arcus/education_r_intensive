# Intro to R and RStudio

<div style="background-color:#e0ffe0;
padding: 1em;
border: 1px solid grey;">

## Overview

This module provides learners with an approachable introduction to the R language and the RStudio IDE, including hands-on practice appropriate for someone who has never used R or RStudio.

**Estimated time to completion**: 1 hour

**Pre-requisites**: It is helpful if learners have used data in a tabular (table-shaped) format, with rows and columns.  Examples of this kind of data include comma separated values files (.csv) and spreadsheets (for example, Microsoft Excel).  Learners do *not* need to have access to R or RStudio on their own computers.

**Learning Objectives**:  After completion of this module, learners will be able to:

* Describe what R is and what RStudio is
* Recognize an R script, open it in RStudio, and run commands
* Explain why using R and RStudio can improve research

</div>

## Content

Feel free to check these off as you go!  

* <input type="checkbox"> :computer: 2 minute preparation for the hands-on activity: [Lesson Preparation](#lesson-preparation)
* <input type="checkbox"> :book: 5 minute read: [What is R?](#what-is-r)
* <input type="checkbox"> :book: 5 minute read: [What is RStudio?](#what-is-rstudio)
* <input type="checkbox"> :computer: 5 minute hands-on activity: [Starting RStudio](#starting-rstudio)
* <input type="checkbox"> :computer: 10 minute hands-on activity: [Using a File](#using-a-file)
* <input type="checkbox"> *Optional* :movie_camera: 10 minute video demonstrating hands-on activities
* <input type="checkbox"> :book: 5 minute read: [Why Use R and RStudio?](#why-use-r-and-rstudio)
* <input type="checkbox"> :computer: 5 minute review of helpful materials in RStudio
* <input type="checkbox"> *Optional* :open_file_folder: Additional Resources:
  - [Why R?] https://www.youtube.com/watch?v=Ids4FO5nTBE&t=07m19s (watch for around 3-4 minutes).  This is a clip from a longer presentation given to learners at the Children's Hospital of Philadelphia.
  - [Cloud Tools for the Unconvinced](https://education.arcus.chop.edu/r-python-cloud/).  This briefly introduces [RStudio.cloud](https://rstudio.cloud) and includes a link to a project you can look at, copy, and learn from.

### Lesson Preparation

If you intend to do the hands on activity in this module, we have a bit of preparation for you to do now.

Because it can take a few minutes for the environment to be created, we suggest you click on the link that will start up the activity.

It will open in a new tab or window, and you can simply return here to continue learning, while the environment finishes loading.

Here's the link.  You don't have to do anything except come back here once the link opens in a new tab or window.

[![Binder](https://binder.pangeo.io/badge_logo.svg)](https://binder.pangeo.io/v2/gh/arcus/education_r_intensive/main?urlpath=rstudio) **← Click the "launch binder" button!**

### What is R?

R is a statistical programming language.  As a programming language, R requires that you write **code** that instructs a computer in what to do.  It's not point-and-click software like Excel or SPSS.

R code looks something like this (you can scroll to the right to see the long url in the second line of consolidate):

```
library(tidyverse)
breast_cancer_data <- read_csv("https://archive.ics.uci.edu/ml/machine-learning-databases/00451/dataR2.csv")
hist(breast_cancer_data$Resistin)
summary(breast_cancer_data$HOMA)
```

Ideally, R code includes helpful hints along the way to help future data users understand what's happening.  We can do that using **comments**, which are lines that the computer knows to ignore and not treat as code.

For example, the following may be a bit easier to understand, even if you are brand new to R:

```
# tidyverse has helpful functions we'll use throughout the analysis

library(tidyverse)

# bring in the data from UCI.

breast_cancer_data <- read_csv("https://archive.ics.uci.edu/ml/machine-learning-databases/00451/dataR2.csv")

# Create a histogram of resistin values

hist(breast_cancer_data$Resistin)

# Show quartiles / mean of HOMA values

summary(breast_cancer_data$HOMA)
```

You can write R code and execute it in many ways, including using the command line, the R console, and in a Jupyter notebook.  Here, however, we're going to concentrate on using RStudio.

[Go back to the table of contents](#content)

### What is RStudio?

RStudio is an **IDE**, or **Integrated Development Environment**, which pulls together (integrates) useful tools like help files, image viewers,  data previews, and version control for people writing (developing) code, and it puts all these tools together in a visually pleasing and helpful environment.  It's an add-on tool that makes working with R easier because it gives extra help and context.

#### What if I Don't Use RStudio?

I could include the code above in a simple **R console**, which is what you get when you install R by itself without using RStudio.  In this example shown below, I'm **not** using RStudio.

|![R.app, or the R Console](https://github.com/arcus/education_r_intensive/blob/main/images/r_console.gif?raw=true)|
|--|

Above, you can see that the R console had to open a new program (in my Mac, it's the Quartz viewer) to display the histogram.  But you can't tell much more about the `breast_cancer_data` datset.  

* What other variables are there?  
* How many rows are in the data?  
* How can I get more information on how to use the `hist` command?
* How can I save my work for later re-use and expansion?

Using the R.app or R console tool means very basic, bare-bones support for you as someone who is trying to write code.

On the other hand, you could run the same code in RStudio and see something like this:

|![RStudio](https://github.com/arcus/education_r_intensive/blob/main/images/rstudio.gif?raw=true)|
|--|

Using RStudio, you:

* can easily create a script to save your code for reuse later (it's currently "Untitled")
* get a sneak peek at the data to help you to decide what to do next (here we have 116 rows of 10 columns)
* see the plot in the same window as everything else
* also have many other helpful tools, like
  - a file browser
  - help tab
  - history of commands you've run recently
  - access to the operating system command line
  - and much more!  

RStudio is the preferred method for most uses of R, and it's generally what we use to teach.

[Go back to the table of contents](#content)

## Starting RStudio

You don't have to have R and RStudio installed on your local computer to learn how to use them.  We've provided a simple environment you can use.  It will probably take a few minutes to load up, especially if it's "cold" (hasn't been used by anyone lately).

Click below and an RStudio environment will open in your browser window.  We suggest using Chrome for this.  Once you click, while you wait for RStudio to load, come back here and read a bit more.

[![Binder](https://binder.pangeo.io/badge_logo.svg)](https://binder.pangeo.io/v2/gh/arcus/education_r_intensive/main?urlpath=rstudio) **← Click the "launch binder" button!**

<div style="background-color:#cceeff;
padding: 1em;
border: 1px solid grey;">

### While You're Waiting...

Do you wonder where you can install R and RStudio, and how much they'll cost your lab?

These are free, open source software (**FOSS**), and both R and RStudio can be installed in a number of different kinds of systems.

You can run R and RStudio:

* from your local computer (download a Windows, Mac, or linux version)
* on a cloud service provider like [RStudio.cloud](https://rstudio.cloud)
* on a server that your research center provides
* on a temporary environment someone prepares for you, like our Pangeo Binder environment

A to-do list for you to consider:

* <input type="checkbox"> Try installing [R](https://cran.rstudio.com/) and [RStudio](https://www.rstudio.com/products/rstudio/download/#download) to your computing device.
* <input type="checkbox"> Not ready to commit to downloading R and RStudio yet?  Create a free [RStudio.cloud](https://rstudio.cloud) account!
* <input type="checkbox"> Ask your colleagues who use R and RStudio where they do their work in R, and if there are any steps you need to take to get access (like request access to a server at your lab or workplace)

</div>

### Still waiting?

While things are loading, you might see an image like this, and it might stay this way for a few minutes.  Be patient!  If you have a few friends to do this together with, it can help speed things up, since the environment will have been recently used and ready to deploy more quickly.

|![Pangeo Load Screen](https://github.com/arcus/education_r_intensive/blob/main/images/pangeo.png?raw=true)|
|--|

### Finally Loaded!

Once your environment has loaded, you will be able to see something like the following:

![RStudio Environment](https://github.com/arcus/education_r_intensive/blob/main/images/rstudio_pangeo.png?raw=true)

Take a look around.  What do you see?  How would you describe the layout of panes and tabs to another person?  What do you think the different parts do?

Try describing RStudio's appearance out loud to yourself.  This may seem silly but it is another way to consolidate your learning.

[Go back to the table of contents](#content)

## Using a File

Before you are ready to write your own code, you might find it useful to work with an existing file.

There are several ways to write R code using RStudio.  We'll start with an R script.  An R script is a text file that includes all the R code and any comments that you want to save in a file so you don't lose track of a process.  For example, let's say that I know I'll want to work on some data stored in a .csv file, and it will take me several days or weeks to slowly write the code.  I'll want to use an R script to store what I've figured out so far.

<div style="background-color:#fefebb;
padding: 1em;
margin: 2em;
border: 1px solid grey;
text-align: center;
font-weight: bolder">

Pro tip:  You'll recognize an R script because it ends in `.R`!</div>

In the lower right of your RStudio window, you should see a pane that has tabs marked "Files", "Plots", "Packages", "Help", and "Viewer".  Click on the "Files" tab and find the R script.  Remember that R scripts end with the file extension `.R`.

Did you find it?  It's called .  Click on the file name and it will open in your "Source" pane, which will appear now that there's an open file.



[Go back to the table of contents](#content)
