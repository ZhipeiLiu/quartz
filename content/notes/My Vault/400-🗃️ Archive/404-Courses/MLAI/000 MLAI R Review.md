## InspectingDataTutorial


Introduction

Statisticians and data analysts need to make sure that they understand the characteristics of data sets that they will work with. Questions they often ask are:

What does one row of the dataset represent?
Who is included in this dataset? Who is not?
What kinds of variables are included?
What data is missing?
Is the data of high-enough quality to use to draw conclusions?
In this tutorial you’ll practice some of the commands you need to use to answer these questions. They’re typically the first commands you run when you encounter a data set you’re not familiar with.

Data for this tutorial

The data for this tutorial is automatically loaded, so you don’t have to use library() to load any packages. (Tutorials are designed for you to quickly practice commands on your own, and the exercises that you’ll do to practice will be embedded in the tutorials themselves. For the weekly labs, however, we will expect you to do the assignments on your own versions of RStudio. )

In case you’re curious, though: we’ll use the ‘mpg’ dataset from the ‘ggplot2’ package in the ‘tidyverse’ collection of packages.

Each row of this dataset is an observation: here there is one observation per distinct manufacturer-model-year-transmission combination.

Each column of this dataset is a variable. A dataset with this structure is called a data frame in R.

The ‘mpg’ data frame has 234 rows and 11 variables.

variables	definition
manufacturer	manufacturer
model	model name
displ	engine displacement, in liters
year	year of manufacture
cyl	number of cylinders
trans	type of transmission
drv	f = front-wheel drive, r = rear wheel drive, 4 = 4wd
cty	city miles per gallon
hwy	highway miles per gallon
fl	fuel type
class	type of car
Viewing a sample of your data

It’s natural to just want to look at your data, and there are some commands in R that let you do that.

In the last tutorial you learned about the View() command in RStudio that lets you take a peek at a data set you load. This is the most common command to use when you’re working on R/RStudio on your own computer, but it won’t work within a tutorial, so to take a peek at a dataset you can use head() or tail(), which show the first or last few rows of a data set. Note that the command View() must be capitalized while the others should not be.



Press the ‘Run Code’ button to see the first few lines of the data for this tutorial. Then you can edit the code to read tail(mpg) instead and press ‘Run Code’ to see the last few lines.
head(mpg)
Initial profiling of data

In practice, though, data sets that you work with in \(\textsf{R}\) may have hundreds of thousands of rows, and so you can’t understand your data well by scrolling through each row and column of the data itself. So the first step data scientists take is to gather summary statistics and plot graphs of different variables. We’ll review the commands to do these things in the first few tutorials.

To get some basic stats on the dimensions of a data frame use the dim() function. (This is short for “dimensions”.) The single argument is the name of a data frame. To find the dimensions of the data frame ‘mpg’ click the ‘Run Code’ button below. The number of rows is given first and then the number of columns.

dim(mpg)
This means that the data frame has 234 rows and 11 columns. If you expected to find more or fewer than 11 variables, or if you felt that you should have more or fewer than 234 observations, this command quickly tells you that your data is not what you expect it to be.

Another useful command to use on a data frame is summary() which gives a quick summary of each column; the only argument is also the name of the data frame. Press the Run Code button below to see the results of the command; more explanation is below.

summary(mpg)
To better understand the output of summary() note that in statistics we generally group variables into one of two broad types: if the possible outcomes for a variable are names we refer to the variable as a categorical variable. If the possible outcomes are things that can be measured, we call it a numeric variable.

If R believes that a variable is numeric, summary() will return summary statistics of that variable. We will see later that sometimes R treats a variable as a number when it is really categorical, so you should trust your assessment of the variables in the dataset more than R.

If R believes that a variable is a string of characters, then summary() will tell you the variable is “Class: character”. This can be useful when you expect a variable to be numeric but R doesn’t recognize it as a number. We’ll later learn how you can fix these issues.

summary() will also tell you how many observations are NA–this is R’s designation for missing data. None of the variables in the ‘mpg’ dataset have missing values, so no NA’s are reported.

Test yourself

For these questions we’ll work with the ‘starwars’ data set that is built into this tutorial. It gives descriptive information about characters in various movies in the Star Wars film franchise.

Enter code in the box below to find the dimensions of the ‘starwars’ dataset. The answer is provided in case you get stuck, but give it a shot on your own first.
dim(starwars)
Question 1

Enter code in the box below to get a summary of variables present in the ‘starwars’ dataset, and then enter the question below. Your answer below may have a lot of white space in between variable summaries.
summary(starwars)
Question 2

The dreaded +

When you run these commands on your own computer you will type them in a script in the upper left pane, and you will see the results in the Console tab in the lower left pane. At the beginning you’ll likely have many errors, and this is normal. The most common are misspellings, not capitalizing correctly, and not having commands loaded with the library() commands.

Another common error is getting just a + returned in the Console tab: if you type and run the command summary(iris in your script (where you leave off the last parenthesis), your Console tab will not give you a summary of the variables in the ‘iris’ data frame, but instead this:



This is your indication that something about your command is unfinished, and R is waiting for you to complete it. To fix this, put your cursor in the Console tab of the lower left pane, right after the +, and press the ESC key. Sometimes this takes a couple of tries, but you should eventually see the ‘>’ command prompt. Then fix your command in your script and rerun it.


## 