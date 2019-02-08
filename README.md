
<!-- README.md is generated from README.Rmd. Please edit that file -->

# feasts

[![Travis build
status](https://travis-ci.org/tidyverts/feasts.svg?branch=master)](https://travis-ci.org/tidyverts/feasts)

The R package *feasts* munches on tidy temporal data
([tsibble](https://github.com/tidyverts/tsibble)) to produce time series
features, decompositions, statistical summaries and convenient
visualisations.

The features offered by *feasts* are essential for the
[fable](https://github.com/tidyverts/fable) modelling workflow. It
includes convenient functions for exploration prior to modelling, and
evaluation after modelling.

## Installation

You can install the development version from
[GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("tidyverts/feasts")
```

## Example

``` r
library(feasts)
library(tsibbledata)
#> Loading required package: tsibble
#> 
#> Attaching package: 'tsibble'
#> The following object is masked from 'package:stats':
#> 
#>     filter
elecdemand %>% 
  ACF(Temperature, lag.max=48) %>%
  autoplot
```

<img src="man/figures/README-acf-1.png" width="100%" />
