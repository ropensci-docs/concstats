# A set of Market Structure, Concentration, and Inequality Measures

A convenience function which calculates a selected set of different
market structure, inequality and concentration measures more or less
commonly used, e.g. k-firm ratios, Entropy, HHI, Palma ratio, and others
in a one step procedure to provide a first overview.

## Usage

``` r
concstats_concstats(x, na.rm = TRUE, digits = NULL)
```

## Arguments

- x:

  A non-negative numeric vector.

- na.rm:

  A logical vector that indicates whether `NA` values should be excluded
  or not. Must be either `TRUE` or `FALSE`. Defaults to `TRUE`. If set
  to `FALSE` the computation yields `NA` if vector contains `NA` values.

- digits:

  A non-null value for digits specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option.

## Value

A `data frame` of numeric measures with default settings from the
respective individual measure.

## Details

`concstats_concstats` computes a set of different and selected
structural, inequality, and concentration measures in a one step
procedure. The resulting `data frame` contains eight measures: number of
firms with market share, numbers equivalent, the cumulative share of the
top (top 3 and top 5) firm(s) in percentage, the hhi index, the entropy
index, and the palma ratio. However, all measures can be computed
individually or in groups.

## Note

The vector of market shares should be in a decimal form corresponding to
the total share of individual firms/units. The vector should sum up to
1, otherwise a numeric vector will be converted into decimal form.

## See also

[`concstats_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_mstruct.md),
[`concstats_comp()`](https://docs.ropensci.org/concstats/reference/concstats_comp.md),
[`concstats_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_inequ.md)

## Examples

``` r
# a vector of market shares
x <- c(0.35, 0.4, 0.05, 0.1, 0.06, 0.04)
# a selected set of different structural, concentration, and inequality
# measures
concstats_concstats(x, digits = 2)
#>          Measure Value
#> 1          Firms  6.00
#> 2 Nrs_equivalent  3.33
#> 3        Top (%) 40.00
#> 4       Top3 (%) 85.00
#> 5       Top5 (%) 96.00
#> 6            HHI  0.30
#> 7        Entropy  0.79
#> 8    Palma ratio  2.67
```
