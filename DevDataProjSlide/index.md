---
title       : Developing Data Products - Course Project
subtitle    : Best Car for Your Trip
author      : Himanshu Singh
job         : Senior Analyst
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

<!-- ## Read-And-Delete -->

<!-- 1. Edit YAML front matter -->
<!-- 2. Write using R Markdown -->
<!-- 3. Use an empty line followed by three dashes to separate slides! -->

<!----- .class #id -->

## Introduction
========================================================
This presentation is part of the Course Project for the Coursera Developing Data Products class. The peer assessed assignment has two parts. First, we need to create a Shiny application and deploy it on Rstudio's servers. Second, we should use Slidify or Rstudio Presenter to prepare a reproducible pitch presentation about the application. This presentation adresses the second part of the course project.

The app developed for the first part of the assignment is available at:
https://himanshus.shinyapps.io/DevDataProdProject/

Source code for ui.R and server.R files are available on the GitHub:
https://github.com/s-himanshu/DevDataProdProject


## <h3 align="center">Enjoy the App! </h2>

---
## Selecting the best Car For Your Road Trip
========================================================
I do not own a car, and if you love road trips, this app is for You!
This app allows to choose the best car for your road trip, based on some simple parameters. It should help you economise fuel consumption to save both money and fuel. This is especially important when your journey spans a few hundred miles or more.
The basic parameters are:
- Distance to Travel
- Fuel Price
- Fuel Budget

Advanced parameters available are:
- Cylinders
- Displacement Volume
- Horse Power
- Transmission Type

---
## Source Data
==============
MTCARS DATASET

The data used in the app comes from the Motor Trend Car Road Tests (mtcars) dataset. The data was extracted from the 1974 Motor Trend US magazine, and comprises fuel consumption and 10 aspects of automobile design and performance for 32 automobiles (1973-74 models). We will look at some features of the data:

```r
head(mtcars)
```

```
##                    mpg cyl disp  hp drat    wt  qsec vs am gear carb
## Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
## Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
## Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
## Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
## Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2
## Valiant           18.1   6  225 105 2.76 3.460 20.22  1  0    3    1
```

---
## Plot 
========================================================
The following plot shows the relationship between three variables: miles per gallon (mpg), displacement volume, and weight of the car. It appears that generally, the higher is the displacement or weight, lower in the mpg.

![plot of chunk Plot](figure/Plot-1.png)
