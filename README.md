
<!-- Don't edit README.md; instead, edit README.Rmd -->

# <img src="https://i.imgur.com/vTLlhbp.png" align="right" height=88 /> Plot ForestGEO-like datasets

[![lifecycle](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![Build
Status](https://travis-ci.org/forestgeo/fgeo.map.svg?branch=master)](https://travis-ci.org/forestgeo/fgeo.map)
[![Coverage
status](https://codecov.io/gh/forestgeo/fgeo.map/branch/master/graph/badge.svg)](https://codecov.io/github/forestgeo/fgeo.map?branch=master)
[![CRAN
status](https://www.r-pkg.org/badges/version/fgeo.map)](https://cran.r-project.org/package=fgeo.map)

## Installation

[Install all **fgeo** packages in one
step](https://forestgeo.github.io/fgeo/index.html#installation)

    # install.packages("devtools")
    devtools::install_github("forestgeo/fgeo.map")

For details on how to install packages from GitHub, see [this
article](https://goo.gl/dQKEeg).

## Example

``` r
library(fgeo.map)

# Small dataset with a few species for quick examples
tree <- subset(fgeo.data::luquillo_tree5_random, sp %in% c("PREMON", "CASARB"))
elevation_list <- fgeo.data::luquillo_elevation

autoplot(sp(tree))

autoplot(sp(tree), point_size = 1, shape = 1)

autoplot(elev(elevation_list))

# Same
autoplot(elev(elevation_list$col))

autoplot(sp_elev(tree, elevation_list))

autoplot(sp_elev(tree, elevation_list$col))

# Customize
p <- autoplot(sp_elev(tree, elevation_list$col), fill = "red")
p

hide_color_legend(p)
```

<img src="man/figures/README-fgeo.map-sp-1.png" width="100%" style="display: block; margin: auto;" /><img src="man/figures/README-fgeo.map-sp-2.png" width="100%" style="display: block; margin: auto;" /><img src="man/figures/README-fgeo.map-sp-3.png" width="100%" style="display: block; margin: auto;" /><img src="man/figures/README-fgeo.map-sp-4.png" width="100%" style="display: block; margin: auto;" /><img src="man/figures/README-fgeo.map-sp-5.png" width="100%" style="display: block; margin: auto;" /><img src="man/figures/README-fgeo.map-sp-6.png" width="100%" style="display: block; margin: auto;" /><img src="man/figures/README-fgeo.map-sp-7.png" width="100%" style="display: block; margin: auto;" /><img src="man/figures/README-fgeo.map-sp-8.png" width="100%" style="display: block; margin: auto;" />

[Get started with
**fgeo**](https://forestgeo.github.io/fgeo/articles/fgeo.html)

## Information

  - [Getting help](SUPPORT.md).
  - [Contributing](CONTRIBUTING.md).
  - [Contributor Code of Conduct](CODE_OF_CONDUCT.md).

## Acknowledgments

For ideas and guidance, thanks to Suzanne Lao, Stuart Davis, Shameema
Jafferjee Esufali, David Kenfack and Anudeep Singh.
