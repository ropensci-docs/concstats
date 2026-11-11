# Gini coefficient

Gini coefficient

## Usage

``` r
concstats_gini(x, normalized = TRUE, na.rm = TRUE, digits = NULL)
```

## Arguments

- x:

  A non-negative numeric vector.

- normalized:

  Logical. Argument specifying whether or not a normalized value is
  required. Must be either `TRUE` or `FALSE`. The default is `TRUE`.

- na.rm:

  A logical vector that indicates whether `NA` values should be excluded
  or not. Must be either `TRUE` or `FALSE`. The default is `TRUE`. If
  set to `FALSE` the computation yields `NA` if `NA` values are present.

- digits:

  An optional value for digits. Specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option. Significant digits defaults to 7. Values
  are restricted between 1 and default value.

## Value

A single numeric value.

## See also

Other Concentration and inequality measures:
[`concstats_all_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_all_inequ.md),
[`concstats_entropy()`](https://docs.ropensci.org/concstats/reference/concstats_entropy.md),
[`concstats_grs()`](https://docs.ropensci.org/concstats/reference/concstats_grs.md),
[`concstats_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_inequ.md),
[`concstats_palma()`](https://docs.ropensci.org/concstats/reference/concstats_palma.md),
[`concstats_simpson()`](https://docs.ropensci.org/concstats/reference/concstats_simpson.md)

## Examples

``` r
# a vector of market shares
x <- c(0.4, 0.2, 0.25, 0.1, 0.05)
concstats_gini(x, normalized = TRUE)
#> [1] 0.425

# a vector with NA values
x <- c(0.4, 0.2, 0.25, 0.1, 0.05, NA)
concstats_gini(x, na.rm = TRUE, digits = 2)
#> `x` has NA values. NAs have been removed for computation.
#> [1] 0.43
```
