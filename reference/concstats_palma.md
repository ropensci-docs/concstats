# Palma ratio

The Palma ratio is an alternative to the Gini index. The ratio focuses
on the differences between those in the top and bottom income brackets.

## Usage

``` r
concstats_palma(x, na.rm = TRUE, digits = NULL)
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

A single numeric measure.

## Details

`concstats_palma` measures the ratio of inequality (normally used with
income inequality) of the top 10 percent to the bottom 40 percent.

## References

Palma, J. G. (2006). "Globalizing Inequality: 'Centrifugal' and
'Centripetal' Forces at Work", DESA Working Paper No. 35.

## See also

Other Concentration and inequality measures:
[`concstats_all_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_all_inequ.md),
[`concstats_entropy()`](https://docs.ropensci.org/concstats/reference/concstats_entropy.md),
[`concstats_gini()`](https://docs.ropensci.org/concstats/reference/concstats_gini.md),
[`concstats_grs()`](https://docs.ropensci.org/concstats/reference/concstats_grs.md),
[`concstats_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_inequ.md),
[`concstats_simpson()`](https://docs.ropensci.org/concstats/reference/concstats_simpson.md)

## Examples

``` r
# a vector of market shares
x <- c(0.4, 0.2, 0.25, 0.1, 0.05)
concstats_palma(x)
#> [1] 2.666667

concstats_palma(x, digits = 2)
#> [1] 2.67

# a vector with NA values
x <- c(0.4, 0.2, 0.25, 0.1, 0.05, NA)
concstats_palma(x, na.rm = FALSE)
#> [1] NA
```
