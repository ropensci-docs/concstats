# Market Structure Measures

Set of different market structure measures to reflect a given market
structure.

## Usage

``` r
concstats_mstruct(x, type = c("firm", "nrs_eq", "top", "top3", "top5",
 "all"), na.rm = TRUE, digits = NULL)
```

## Arguments

- x:

  A non-negative numeric vector.

- type:

  A character string of the measure to be calculated, can be abbreviated
  with the first letter. Defaults to "firm". Input is not
  case-sensitive.

- na.rm:

  A logical vector that indicates whether `NA` values should be excluded
  or not. Must be either `TRUE` or `FALSE`. The default is `TRUE`. If
  set to `TRUE` the computation yields a message if the vector contains
  `NA` values. NAs will be removed for further computations. If set to
  `FALSE` with NAs present the computation yield `NA`.

- digits:

  A non-null value for digits specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option. Significant digits defaults to 7. Values
  are restricted between 1 and default value.

## Value

A single calculated numeric measure or `data frame`.

## Details

- `concstats_mstruct` is a wrapper for the proposed structural measures.

- [`concstats_firm()`](https://docs.ropensci.org/concstats/reference/concstats_firm.md),
  returns the number of firms with a given market share.

- [`concstats_nrs_eq()`](https://docs.ropensci.org/concstats/reference/concstats_nrs_eq.md)
  computes the reciprocal of the HHI, which indicates the equivalent
  number of firms of the same size.

- [`concstats_top()`](https://docs.ropensci.org/concstats/reference/concstats_top.md),
  [`concstats_top3()`](https://docs.ropensci.org/concstats/reference/concstats_top3.md),
  and
  [`concstats_top5()`](https://docs.ropensci.org/concstats/reference/concstats_top5.md)
  calculate the cumulative share of the top (top 3 and top 5) firm(s)
  and returns the value in percentage.

- [`concstats_all_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_all_mstruct.md)
  computes all measures in a one step procedure. All measures can be
  computed individually.

- [`concstats_top_df()`](https://docs.ropensci.org/concstats/reference/concstats_top_df.md),
  [`concstats_top3_df()`](https://docs.ropensci.org/concstats/reference/concstats_top3_df.md),
  and
  [`concstats_top5_df()`](https://docs.ropensci.org/concstats/reference/concstats_top5_df.md)
  are slight variations. Firm id or ranking might be of interest. In
  this case an additional id or firm variable is needed. The functions
  will return a data frame. These functions are just individually
  accessible.

## Note

The vector of market shares should be in a decimal form corresponding to
total shares of individual firms/units.The sum of the vector should sum
up to 1. Alternatively, the user might use
[`concstats_shares()`](https://docs.ropensci.org/concstats/reference/concstats_shares.md)
to converting raw variables, e.g. loans or sales into shares.

## See also

[`concstats_concstats()`](https://docs.ropensci.org/concstats/reference/concstats_concstats.md),[`concstats_comp()`](https://docs.ropensci.org/concstats/reference/concstats_comp.md),[`concstats_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_inequ.md)

Other Market structure measures:
[`concstats_all_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_all_mstruct.md),
[`concstats_firm()`](https://docs.ropensci.org/concstats/reference/concstats_firm.md),
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
x <- c(0.35, 0.4, 0.05, 0.1, 0.06, 0.04)
concstats_mstruct(x, type = "firm", digits = 1)
#> [1] 6

# Calculate the market structure group measures
concstats_mstruct(x, type = "all", digits = 2)
#>          Measure     Value
#> 1          Firms  6.000000
#> 2 Nrs_equivalent  3.331113
#> 3        Top (%) 40.000000
#> 4       Top3 (%) 85.000000
#> 5       Top5 (%) 96.000000
```
