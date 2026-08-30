# Dual of the Herfindahl-Hirschman Index

The dual of the HHI reflects the fraction of participants that do have
market participation.

## Usage

``` r
concstats_hhi_d(x, na.rm = TRUE, digits = NULL)
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

  A non-null value for digits specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option.

## Value

A single numeric value.

## Details

`concstats_hhi_d` is the dual of the HHI index, which indicates the
percentage which represents the fraction of the banks that do not have
market participation.

## References

Chang, E. J., Guerra, S. M., de Souza Penaloza, R. A. & Tabak, B. M.
(2005) Banking concentration: the Brazilian case. *In Financial
Stability Report*. Brasilia: Banco Central do Brasil, 4: 109-129.

## See also

Other Competition/Concentration measures:
[`concstats_all_comp()`](https://docs.ropensci.org/concstats/reference/concstats_all_comp.md),
[`concstats_comp()`](https://docs.ropensci.org/concstats/reference/concstats_comp.md),
[`concstats_dom()`](https://docs.ropensci.org/concstats/reference/concstats_dom.md),
[`concstats_hhi()`](https://docs.ropensci.org/concstats/reference/concstats_hhi.md),
[`concstats_hhi_min()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_min.md),
[`concstats_sten()`](https://docs.ropensci.org/concstats/reference/concstats_sten.md)

## Examples

``` r
# a vector of market shares
x <- c(0.35, 0.4, 0.05, 0.1, 0.06, 0.04)
concstats_hhi_d(x)
#> [1] 0.4448146

# a vector with NA values
x <- c(0.4, 0.2, 0.25, 0.1, 0.05, NA)
concstats_hhi_d(x, na.rm = TRUE, digits = 2)
#> `x` has NA values. NAs have been removed for computation.
#> [1] 0.27
```
