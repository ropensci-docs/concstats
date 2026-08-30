# Top market share

Top market share

## Usage

``` r
concstats_top(x, na.rm = TRUE, digits = NULL)
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

A positive numeric value, which indicates the top market share in
percent.

## See also

Other Market structure measures:
[`concstats_all_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_all_mstruct.md),
[`concstats_firm()`](https://docs.ropensci.org/concstats/reference/concstats_firm.md),
[`concstats_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_mstruct.md),
[`concstats_nrs_eq()`](https://docs.ropensci.org/concstats/reference/concstats_nrs_eq.md),
[`concstats_top3()`](https://docs.ropensci.org/concstats/reference/concstats_top3.md),
[`concstats_top3_df()`](https://docs.ropensci.org/concstats/reference/concstats_top3_df.md),
[`concstats_top5()`](https://docs.ropensci.org/concstats/reference/concstats_top5.md),
[`concstats_top5_df()`](https://docs.ropensci.org/concstats/reference/concstats_top5_df.md),
[`concstats_top_df()`](https://docs.ropensci.org/concstats/reference/concstats_top_df.md)

## Examples

``` r
# a vector of market shares
x <- c(0.4, 0.2, 0.25, 0.1, 0.05)
concstats_top(x, digits = 2)
#> [1] 40
```
