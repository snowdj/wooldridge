

[![CRAN_Status_Badge](https://www.r-pkg.org/badges/version/wooldridge)](https://cran.r-project.org/package=wooldridge)
[![status](https://tinyverse.netlify.com/badge/wooldridge)](https://CRAN.R-project.org/package=wooldridge)
[![Travis](https://travis-ci.org/JustinMShea/wooldridge.svg?branch=master)](https://travis-ci.org/JustinMShea/wooldridge) [![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/github/JustinMShea/wooldridge?branch=master&svg=true)](https://ci.appveyor.com/project/JustinMShea/wooldridge)   [![](https://cranlogs.r-pkg.org/badges/wooldridge)](https://CRAN.R-project.org/package=wooldridge)

# wooldridge: 111 Data Sets for Econometrics 

Economics students new to both econometrics and **R** may find the introduction to both challenging. However, if their text is **"Introductory Econometrics: A Modern Approach, 6e"** by Jeffrey M. Wooldridge, they are in luck!

The `wooldridge` package aims to lighten the task by easily loading any data set from the text. The package contains full documentation for each set and all data have been compressed to a fraction of their original size. Just install the package, load it, and call the data you wish to work with.

_**But wait...there's more!**_ A vignette, [Introductory Econometrics Examples](https://justinmshea.github.io/wooldridge/articles/Introductory-Econometrics-Examples.html):sparkles:, illustrates solutions to examples from each chapter of the text, offering a relevant introduction to econometric modelling with **R**. The vignette also includes an Appendix of helpful resources, such as *Using R for Introductory Econometrics* by Florian Hess.


While the original course companion site provides publicly available data sets for Eviews, Excel, and Stata commercial software, this package is the **official R open source option**. Using **R** while building a foundation in econometric modeling, not only saves learners a few units of currency, but also introduces them to software capable of scaling with the demands of modern statistical computing.

**Note:** All data sets are from the 6th edition (Wooldridge 2016, `ISBN-13: 978-1-305-27010-7`), which is compatible with all other editions.


## Installation


One can Install `wooldridge` directly from The Comprehensive R Archive Network (**CRAN**), which depends on **R >= 3.2.0**.


```{r}
install.packages("wooldridge")
```
## Documentation 

It's always recommended that one read supporting documentation for data sets of interest. This becomes trivial with the `wooldridge` package:

```{r}
?wage1
```

Documentation includes Wooldridge's original **source**, data **format**, variable names and their descriptions, as well as page numbers where each set is referenced in the text. Some sets even contain additional **notes** suggesting related research projects or exploration.

## Example

Load the `wooldridge` package and use the `data()` function to bring the desired data set into the working environment. Data set names match those in the text. Once present in the working environment, modelling data is quick and easy, leaving learners with more time to focus on interpretation of results and general diagnostics.

```{r}
library(wooldridge)

data("wage1")

wageModel <- lm(lwage ~ educ + exper + tenure, data = wage1)

summary(wageModel)
```




