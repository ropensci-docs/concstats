# Herfindahl-Hirschman Index

A measure of industry concentration and widely used in merger control.

## Usage

``` r
concstats_hhi(x, normalized = FALSE, na.rm = TRUE, digits = NULL)
```

## Arguments

- x:

  A non-negative numeric vector.

- normalized:

  Logical. Argument specifying whether or not a normalized value is
  required. Must be either `TRUE` or `FALSE`. The default is `FALSE`.

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

`concstats_hhi` calculates the widely used Herfindahl-Hirschman Index
(Herfindahl, 1950 and Hirschman, 1945). The index is calculated by
squaring the market share of each firm competing in the market and then
summing the resulting numbers.

## References

Herfindahl, O. C. (1950), "Concentration in the steel industry" (PhD
thesis), Columbia University.

Hirschman, A. O. (1945), "National power and structure of foreign
trade". Berkeley, CA: University of California Press.

## See also

Other Competition/Concentration measures:
[`concstats_all_comp()`](https://docs.ropensci.org/concstats/reference/concstats_all_comp.md),
[`concstats_comp()`](https://docs.ropensci.org/concstats/reference/concstats_comp.md),
[`concstats_dom()`](https://docs.ropensci.org/concstats/reference/concstats_dom.md),
[`concstats_hhi_d()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_d.md),
[`concstats_hhi_min()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_min.md),
[`concstats_sten()`](https://docs.ropensci.org/concstats/reference/concstats_sten.md)

## Examples

``` r
# a vector of market shares
x <- c(0.35, 0.4, 0.05, 0.1, 0.06, 0.04)
concstats_hhi(x, digits = 2)
#> [1] 0.3

# a vector with NA values
x <- c(0.4, 0.2, 0.25, 0.1, 0.05, NA)
concstats_hhi(x, na.rm = TRUE)
#> `x` has NA values. NAs have been removed for computation.
#> [1] 0.275
```
