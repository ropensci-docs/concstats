# Shannon Entropy

Shannon Entropy

## Usage

``` r
concstats_entropy(x, normalized = TRUE, na.rm = TRUE, digits = NULL)
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
  will use base R print option.

## Value

A single numeric measure.

## References

Shannon, C. E. (1948). "A Mathematical Theory of Communication", *The
Bell System Technical Journal* (Nokia Bell Labs).

## See also

Other Concentration and inequality measures:
[`concstats_all_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_all_inequ.md),
[`concstats_gini()`](https://docs.ropensci.org/concstats/reference/concstats_gini.md),
[`concstats_grs()`](https://docs.ropensci.org/concstats/reference/concstats_grs.md),
[`concstats_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_inequ.md),
[`concstats_palma()`](https://docs.ropensci.org/concstats/reference/concstats_palma.md),
[`concstats_simpson()`](https://docs.ropensci.org/concstats/reference/concstats_simpson.md)

## Examples

``` r
# a vector of market shares
x <- c(0.4, 0.2, 0.25, 0.1, 0.05)
concstats_entropy(x, normalized = TRUE)
#> [1] 0.879203

# a vector with NA values
x <- c(0.4, 0.2, 0.25, 0.1, 0.05, NA)
concstats_entropy(x, na.rm = TRUE, digits = 2)
#> `x` has NA values. NAs have been removed for computation.
#> [1] 0.88
```
