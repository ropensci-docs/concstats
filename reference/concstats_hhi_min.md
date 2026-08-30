# Minimum of Herfindahl-Hirschman Index

Minimum of Herfindahl-Hirschman Index

## Usage

``` r
concstats_hhi_min(x, na.rm = TRUE, digits = NULL)
```

## Arguments

- x:

  A non-negative numeric vector.

- na.rm:

  A logical vector that indicates whether `NA` values should be excluded
  or not. Must be either `TRUE` or `FALSE`. The default is `TRUE`. If
  set to `FALSE` the computation yields a message if the vector contains
  `NA` values. NAs will be removed for further computations.

- digits:

  A non-null value for digits specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option.

## Value

A single numeric measure in decimal form.

## Details

Calculates the minimum of the Herfindahl-Hirschman index, that is, the
equivalent of all participants in the market with equal market shares.

## See also

Other Competition/Concentration measures:
[`concstats_all_comp()`](https://docs.ropensci.org/concstats/reference/concstats_all_comp.md),
[`concstats_comp()`](https://docs.ropensci.org/concstats/reference/concstats_comp.md),
[`concstats_dom()`](https://docs.ropensci.org/concstats/reference/concstats_dom.md),
[`concstats_hhi()`](https://docs.ropensci.org/concstats/reference/concstats_hhi.md),
[`concstats_hhi_d()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_d.md),
[`concstats_sten()`](https://docs.ropensci.org/concstats/reference/concstats_sten.md)

## Examples

``` r
# a vector of market shares
x <- c(0.35, 0.4, 0.05, 0.1, 0.06, 0.04)
concstats_hhi_min(x, digits = 2)
#> [1] 0.17

# a vector with NA values
x <- c(0.4, 0.2, 0.25, 0.1, 0.05, NA)
concstats_hhi_min(x, na.rm = FALSE)
#> [1] NA
```
