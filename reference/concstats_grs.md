# GRS measure

GRS measure

## Usage

``` r
concstats_grs(x, na.rm = TRUE, digits = NULL)
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

  An optional value for digits. Specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option.

## Value

A single numeric value.

## References

Ginevicius, R. and S. Cirba (2009). "Additive measurement of market
concentration", *Journal of Business Economics and Management*, 10(3),
191-198.

## See also

Other Concentration and inequality measures:
[`concstats_all_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_all_inequ.md),
[`concstats_entropy()`](https://docs.ropensci.org/concstats/reference/concstats_entropy.md),
[`concstats_gini()`](https://docs.ropensci.org/concstats/reference/concstats_gini.md),
[`concstats_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_inequ.md),
[`concstats_palma()`](https://docs.ropensci.org/concstats/reference/concstats_palma.md),
[`concstats_simpson()`](https://docs.ropensci.org/concstats/reference/concstats_simpson.md)

## Examples

``` r

# a vector of market shares
x <- c(0.4, 0.3, 0.2, 0.1)
concstats_grs(x, digits = 3)
#> [1] 0.398
#[1] 0.398

# a vector with NA values
x <- c(0.4, 0.2, 0.25, 0.1, 0.05, NA)
concstats_grs(x, na.rm = FALSE)
#> [1] NA
```
