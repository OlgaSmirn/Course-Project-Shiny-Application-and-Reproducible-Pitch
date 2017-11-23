Course Project:   Shiny Application and Reproducible Pitch
========================================================
author:  Olga Smirnov
date:    11/19/2017
autosize: true

Overview
========================================================

The presended application may be used to predict the diamond price based on historical price information.

The aplication is developed as an assignment for the course Developing Data Products (part of the Coursera Data Science Specialization).

Data used
========================================================
The application uses information about ~54,000 round diamonds from http://www.diamondse.info/

Dataset includes:
* Diamond price
* Carat, colour, cut (these data is used for prediction)
* Total depth, clarity, table, depth, width, height (these data is NOT used in presented application)


Prediction model
========================================================

Application uses simple linear model to predict diamond price based on its characteristics.

Here is the sample of prediction of price for 1 carat diamond ingoring all other characteristics:


```r
library(ggplot2)
car <- 1

diam <- diamonds[,c(1:3,7)]
fit <- lm(price~carat, diam)
pred <- predict(fit, newdata = data.frame(carat = car))  
paste(round(pred, digits = 2), "$")
```

```
[1] "5500.07 $"
```

========================================================

The application is avalilable at: https://mysite.shinyapps.io/course9week4/

Source code is located in the GitHub repo: https://github.com/OlgaSmirn/Course-Project-Shiny-Application-and-Reproducible-Pitch/tree/master

