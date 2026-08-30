# Gini-Simpson Index

Gini-Simpson Index

## Usage

``` r
concstats_simpson(x, na.rm = TRUE, digits = NULL)
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

A single numeric value in decimal form.

## Details

`concstats_simpson` is the Gini-Simpson index, also known as the Gini
impurity (Gini's diversity index) in Machine Learning, Gibbs-Martin
index or Blau index in sociology and management studies. This index
ranges from {0, 1}.

## References

Simpson, E. H. (1949). "Measurement of Diversity", *Nature*, 163, 688.

Jost, L. (2006). "Entropy and Diversity". *Oikos*, 113(2), 363-375.

## See also

Other Concentration and inequality measures:
[`concstats_all_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_all_inequ.md),
[`concstats_entropy()`](https://docs.ropensci.org/concstats/reference/concstats_entropy.md),
[`concstats_gini()`](https://docs.ropensci.org/concstats/reference/concstats_gini.md),
[`concstats_grs()`](https://docs.ropensci.org/concstats/reference/concstats_grs.md),
[`concstats_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_inequ.md),
[`concstats_palma()`](https://docs.ropensci.org/concstats/reference/concstats_palma.md)

## Examples

``` r
# a vector of market shares
x <- c(0.4, 0.2, 0.25, 0.1, 0.05)
concstats_simpson(x)
#> [1] 0.725

concstats_simpson(x, digits = 2)
#> [1] 0.72

# a vector with NA values
x <- c(0.4, 0.2, 0.25, 0.1, 0.05, NA)
concstats_simpson(x, na.rm = TRUE)
#> `x` has NA values. NAs have been removed for computation.
#> [1] 0.725
```
