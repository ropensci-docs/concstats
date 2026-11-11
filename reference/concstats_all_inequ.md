# A wrapper for the proposed inequality measures

A wrapper for the proposed inequality measures

## Usage

``` r
concstats_all_inequ(x, normalized = TRUE, na.rm = TRUE, digits = NULL)
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
  set to `FALSE` the computation yields `NA` if `NA` values are present.

- digits:

  An optional value for digits. Specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option.

## Value

A `data.frame`.

## Details

`concstats_all_inequ` returns all proposed group measures in a one step
procedure with default settings if not otherwise specified.

## See also

[`concstats_all_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_all_mstruct.md),
[`concstats_all_comp()`](https://docs.ropensci.org/concstats/reference/concstats_all_comp.md)

Other Concentration and inequality measures:
[`concstats_entropy()`](https://docs.ropensci.org/concstats/reference/concstats_entropy.md),
[`concstats_gini()`](https://docs.ropensci.org/concstats/reference/concstats_gini.md),
[`concstats_grs()`](https://docs.ropensci.org/concstats/reference/concstats_grs.md),
[`concstats_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_inequ.md),
[`concstats_palma()`](https://docs.ropensci.org/concstats/reference/concstats_palma.md),
[`concstats_simpson()`](https://docs.ropensci.org/concstats/reference/concstats_simpson.md)

## Examples

``` r
# a vector of market shares
x <- c(0.35, 0.4, 0.05, 0.1, 0.06, 0.04)
concstats_all_inequ(x, digits = 2)
#>         Measure Value
#> 1       Entropy  0.79
#> 2    Gini Index  0.55
#> 3 Simpson Index  0.70
#> 4   Palma Ratio  2.67
#> 5           GRS  0.40
```
