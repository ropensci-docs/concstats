# Inequality and Diversity Measures

A set of different inequality and diversity measures.

## Usage

``` r
concstats_inequ(x, normalized = TRUE, type = c("entropy", "gini",
 "simpson", "palma", "grs", "all"), na.rm = TRUE, digits = NULL)
```

## Arguments

- x:

  A non-negative numeric vector.

- normalized:

  Logical. Argument of the functions `concstats_entropy`,
  `concstats_gini` specifying whether or not a normalized value is
  required. Must be either `TRUE` or `FALSE`. The default is `TRUE`.

- type:

  A character string of the measure to be calculated, defaults to
  `concstats_entropy`. Input is not case-sensitive.

- na.rm:

  A logical vector that indicates whether `NA` values should be excluded
  or not. Must be either `TRUE` or `FALSE`. The default is `TRUE`. If
  set to `FALSE` the computation yields a message if the vector contains
  `NA` values. NAs will be removed for further computations.

- digits:

  A non-null value for digits specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option. Significant digits defaults to 7. Values
  are restricted between 1 and default value.

## Value

The calculated numeric measure or a `data frame`

## Details

- `concstats_inequ` is a wrapper for the proposed inequality measures.
  All measures can be accessed individually.

- [`concstats_entropy()`](https://docs.ropensci.org/concstats/reference/concstats_entropy.md)
  returns the Shannon entropy. `concstats_entropy` You can normalize the
  entropy measures by setting `normalized = TRUE`.

- [`concstats_gini()`](https://docs.ropensci.org/concstats/reference/concstats_gini.md)
  calculates the gini coefficient. `concstats_gini` You can normalize
  the gini measures by setting `normalized = TRUE`.

- [`concstats_simpson()`](https://docs.ropensci.org/concstats/reference/concstats_simpson.md)
  calculates the gini-simpson index.

- [`concstats_palma()`](https://docs.ropensci.org/concstats/reference/concstats_palma.md)
  calculates the palma ratio of inequality.

- [`concstats_grs()`](https://docs.ropensci.org/concstats/reference/concstats_grs.md)
  calculates an alternative concentration measure.

- [`concstats_all_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_all_inequ.md)
  returns all measures in a one step procedure. For more details or
  references please see the help page of the respective function.

## See also

[`concstats_concstats()`](https://docs.ropensci.org/concstats/reference/concstats_concstats.md),[`concstats_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_mstruct.md),[`concstats_comp()`](https://docs.ropensci.org/concstats/reference/concstats_comp.md)

Other Concentration and inequality measures:
[`concstats_all_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_all_inequ.md),
[`concstats_entropy()`](https://docs.ropensci.org/concstats/reference/concstats_entropy.md),
[`concstats_gini()`](https://docs.ropensci.org/concstats/reference/concstats_gini.md),
[`concstats_grs()`](https://docs.ropensci.org/concstats/reference/concstats_grs.md),
[`concstats_palma()`](https://docs.ropensci.org/concstats/reference/concstats_palma.md),
[`concstats_simpson()`](https://docs.ropensci.org/concstats/reference/concstats_simpson.md)

## Examples

``` r
# a vector of market shares
x <- c(0.4, 0.2, 0.25, 0.1, 0.05)

# Calculate the Palma ratio
concstats_inequ(x, type = "palma")
#> [1] 2.666667

# Calculate the entropy measure directly
concstats_inequ(x, normalized = TRUE, type = "entropy")
#> [1] 0.879203

# Calculate the group measures
concstats_inequ(x, type = "all", digits = 2)
#>         Measure Value
#> 1       Entropy  0.88
#> 2    Gini Index  0.43
#> 3 Simpson Index  0.72
#> 4   Palma Ratio  2.67
#> 5           GRS  0.40
```
