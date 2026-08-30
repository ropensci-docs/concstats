# Dominance Index

An alternative measure which can be used in case of mergers.

## Usage

``` r
concstats_dom(x, na.rm = TRUE, digits = NULL)
```

## Arguments

- x:

  A non-negative numeric vector.

- na.rm:

  A logical vector that indicates whether `NA` values should be excluded
  or not. Must be either `TRUE` or `FALSE`. The default is `TRUE`. If
  set to `FALSE` the computation yields a warning if the vector contains
  `NA` values. NAs will be removed for further computations.

- digits:

  An optional value for digits. Specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option.

## Value

A single numeric measure in decimal form or, if NAs are present, with a
warning.

## Details

`concstats_dom` calculates a dominance index, which measures the
concentration within the Herfindahl-Hirschman index, that is, the
concentration within the concentration.

## References

Garcia Alba Idunate, P. (1994). "Un Indice de dominancia para el
analisis de la estructura de los mercados". *El Trimestre Economico*,
61: 499-524.

## See also

Other Competition/Concentration measures:
[`concstats_all_comp()`](https://docs.ropensci.org/concstats/reference/concstats_all_comp.md),
[`concstats_comp()`](https://docs.ropensci.org/concstats/reference/concstats_comp.md),
[`concstats_hhi()`](https://docs.ropensci.org/concstats/reference/concstats_hhi.md),
[`concstats_hhi_d()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_d.md),
[`concstats_hhi_min()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_min.md),
[`concstats_sten()`](https://docs.ropensci.org/concstats/reference/concstats_sten.md)

## Examples

``` r
# a vector of market shares
x <- c(0.35, 0.4, 0.05, 0.1, 0.06, 0.04)
concstats_dom(x, na.rm = FALSE, digits = 2)
#> [1] 0.45

# a vector with NA values
x <- c(0.4, 0.2, 0.25, 0.1, 0.05, NA)
concstats_dom(x, digits = 2)
#> `x` has NA values. NAs have been removed for computation.
#> [1] 0.41
```
