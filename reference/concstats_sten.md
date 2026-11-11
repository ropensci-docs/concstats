# Stenbacka Index

The measure suggests an approach that classifies when an individual firm
has a dominant position and therefore assesses market dominance.

## Usage

``` r
concstats_sten(x, na.rm = TRUE, digits = NULL)
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

A single numeric measure in decimal form.

## Details

`concstats_sten` calculates the Stenbacka index, which indicates the
market share of a dominant position.

## References

Melnik, A., Shy, Oz, Stenbacka, R., (2008), "Assessing market
dominance", *Journal of Economic Behavior and Organization*, 68: pp.
63-72.

## See also

Other Competition/Concentration measures:
[`concstats_all_comp()`](https://docs.ropensci.org/concstats/reference/concstats_all_comp.md),
[`concstats_comp()`](https://docs.ropensci.org/concstats/reference/concstats_comp.md),
[`concstats_dom()`](https://docs.ropensci.org/concstats/reference/concstats_dom.md),
[`concstats_hhi()`](https://docs.ropensci.org/concstats/reference/concstats_hhi.md),
[`concstats_hhi_d()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_d.md),
[`concstats_hhi_min()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_min.md)

## Examples

``` r
# a vector of market shares
x <- c(0.35, 0.4, 0.05, 0.1, 0.06, 0.04)
concstats_sten(x, digits = 2)
#> [1] 48.12

concstats_sten(x, digits = 3)
#> [1] 48.125

# a vector with NA values
x <- c(0.4, 0.2, 0.25, 0.1, 0.05, NA)
concstats_sten(x, na.rm = TRUE)
#> `x` has NA values. NAs have been removed for computation.
#> [1] 45.125
```
