# A wrapper for the proposed concentration measures

A wrapper for the proposed concentration measures

## Usage

``` r
concstats_all_comp(x, normalized = FALSE, na.rm = TRUE, digits = NULL)
```

## Arguments

- x:

  A non-negative numeric vector. The computation yields `NA` if `NA`
  values are present.

- normalized:

  Logical. Argument specifying whether or not a normalized value is
  required. Must be either `TRUE` or `FALSE`. Defaults to `FALSE`.

- na.rm:

  A logical vector that indicates whether `NA` values should be excluded
  or not. Must be either `TRUE` or `FALSE`. The default is `TRUE`. If
  set to `FALSE` the computation yields `NA` if vector contains `NA`
  values.

- digits:

  An optional value for digits. Specifies the minimum number of
  significant digits to be printed in values.

## Value

A `data.frame`.

## Details

`concstats_all_comp` returns all proposed group measures in a one step
procedure with default settings if not otherwise specified.

## See also

[`concstats_all_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_all_mstruct.md),
[`concstats_all_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_all_inequ.md)

Other Competition/Concentration measures:
[`concstats_comp()`](https://docs.ropensci.org/concstats/reference/concstats_comp.md),
[`concstats_dom()`](https://docs.ropensci.org/concstats/reference/concstats_dom.md),
[`concstats_hhi()`](https://docs.ropensci.org/concstats/reference/concstats_hhi.md),
[`concstats_hhi_d()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_d.md),
[`concstats_hhi_min()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_min.md),
[`concstats_sten()`](https://docs.ropensci.org/concstats/reference/concstats_sten.md)

## Examples

``` r
# a vector of market shares
x <- c(0.35, 0.4, 0.05, 0.1, 0.06, 0.04)
concstats_all_comp(x, digits = 2)
#>        Measure Value
#> 1          HHI  0.30
#> 2     HHI(min)  0.17
#> 3    HHI(dual)  0.44
#> 4    Dominance  0.45
#> 5 Stenbacka(%) 48.12
```
