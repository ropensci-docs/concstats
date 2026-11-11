# Top 5 market shares data frame

Top 5 market shares data frame

## Usage

``` r
concstats_top5_df(x, y, digits = NULL)
```

## Arguments

- x:

  A data frame or tibble.

- y:

  A non-negative vector of shares. All integers (e.g. sales) are
  converted to relative decimal numbers.

- digits:

  An optional value for digits. Specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option. Significant digits defaults to 7. Values
  are restricted between 1 and default value.

## Value

A `data frame`.

## Note

Note that the first column in your data frame will be the index and
values should be unique.

## See also

Other Market structure measures:
[`concstats_all_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_all_mstruct.md),
[`concstats_firm()`](https://docs.ropensci.org/concstats/reference/concstats_firm.md),
[`concstats_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_mstruct.md),
[`concstats_nrs_eq()`](https://docs.ropensci.org/concstats/reference/concstats_nrs_eq.md),
[`concstats_top()`](https://docs.ropensci.org/concstats/reference/concstats_top.md),
[`concstats_top3()`](https://docs.ropensci.org/concstats/reference/concstats_top3.md),
[`concstats_top3_df()`](https://docs.ropensci.org/concstats/reference/concstats_top3_df.md),
[`concstats_top5()`](https://docs.ropensci.org/concstats/reference/concstats_top5.md),
[`concstats_top_df()`](https://docs.ropensci.org/concstats/reference/concstats_top_df.md)

## Examples

``` r
x <- data.frame(
firm = c("A", "B", "C", "D", "E"),
share = c(0.2,0.25,0.1,0.05,0.4)
)
concstats_top5_df(x, "share", digits = 2)
#> # A tibble: 5 × 2
#>   firm  share
#>   <chr> <dbl>
#> 1 E        40
#> 2 B        25
#> 3 A        20
#> 4 C        10
#> 5 D         5
```
