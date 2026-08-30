# A wrapper for the proposed structural measures

A wrapper for the proposed structural measures

## Usage

``` r
concstats_all_mstruct(x, na.rm = TRUE, digits = NULL)
```

## Arguments

- x:

  A non-negative numeric vector.

- na.rm:

  A logical vector that indicates whether `NA` values should be excluded
  or not. Must be either `TRUE` or `FALSE`. The default is `TRUE`. If
  set to `FALSE` the computation yields `NA` if the vector contains `NA`
  values.

- digits:

  An optional value for digits. Specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option.

## Value

A `data.frame`.

## Details

`concstats_all_mstruct` returns all proposed group measures in a one
step procedure with default settings if not otherwise specified.

## See also

[`concstats_all_comp()`](https://docs.ropensci.org/concstats/reference/concstats_all_comp.md),
[`concstats_all_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_all_inequ.md)

Other Market structure measures:
[`concstats_firm()`](https://docs.ropensci.org/concstats/reference/concstats_firm.md),
[`concstats_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_mstruct.md),
[`concstats_nrs_eq()`](https://docs.ropensci.org/concstats/reference/concstats_nrs_eq.md),
[`concstats_top()`](https://docs.ropensci.org/concstats/reference/concstats_top.md),
[`concstats_top3()`](https://docs.ropensci.org/concstats/reference/concstats_top3.md),
[`concstats_top3_df()`](https://docs.ropensci.org/concstats/reference/concstats_top3_df.md),
[`concstats_top5()`](https://docs.ropensci.org/concstats/reference/concstats_top5.md),
[`concstats_top5_df()`](https://docs.ropensci.org/concstats/reference/concstats_top5_df.md),
[`concstats_top_df()`](https://docs.ropensci.org/concstats/reference/concstats_top_df.md)

## Examples

``` r
# a vector of market shares
x <- c(0.4, 0.2, 0.25, 0.1, 0.05)
concstats_all_mstruct(x, digits = 2)
#>          Measure Value
#> 1          Firms   5.0
#> 2 Nrs_equivalent   3.6
#> 3        Top (%)  40.0
#> 4       Top3 (%)  85.0
#> 5       Top5 (%) 100.0
```
