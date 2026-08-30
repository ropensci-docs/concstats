# Group of Concentration Measures

A set of different concentration and competition measures.

## Usage

``` r
concstats_comp(x, normalized = FALSE, type = c("hhi", "hhi_d", "hhi_min",
 "dom", "sten", "all"), na.rm = TRUE, digits = NULL)
```

## Arguments

- x:

  A non-negative numeric vector.

- normalized:

  Logical. Argument specifying whether or not a normalized value is
  required. Ranges from {0, 1} and often used for comparison over time.
  Must be either `TRUE` or `FALSE`. The default is `FALSE`.

- type:

  A character string of the measure to be calculated, can be abbreviated
  with the first letter. Defaults to "hhi". Input is not case-sensitive.

- na.rm:

  A logical vector that indicates whether `NA` values should be excluded
  or not. If set to `FALSE` the computation yields `NA` if vector
  contains `NA` values. Must be either `TRUE` or `FALSE`. Defaults to
  `TRUE` and NAs will be removed for further computations with a
  message.

- digits:

  A non-null value for digits specifies the minimum number of
  significant digits to be printed in values. The default is `NULL` and
  will use base R print option. Significant digits defaults to 7. Values
  are restricted between 1 and default value.

## Value

A single numeric measure in decimal form or `data frame`.

## Details

- `concstats_comp` is a wrapper for the proposed concentration measures.
  All measures can be accessed individually.

- [`concstats_hhi()`](https://docs.ropensci.org/concstats/reference/concstats_hhi.md)
  returns the Herfindahl-Hirschman index (HHI). `concstats_hhi`, can be
  calculated individually as a normalized measure changing the default
  setting to `TRUE`.

- [`concstats_hhi_d()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_d.md)
  returns the dual of the HHI.

- [`concstats_hhi_min()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_min.md)
  calculates the minimum of the HHI index.

- [`concstats_dom()`](https://docs.ropensci.org/concstats/reference/concstats_dom.md)
  calculates the dominance index.

- [`concstats_sten()`](https://docs.ropensci.org/concstats/reference/concstats_sten.md)
  calculates the stenbacka index.

- [`concstats_all_comp()`](https://docs.ropensci.org/concstats/reference/concstats_all_comp.md)
  is a wrapper that computes all measures in a one step procedure. For
  more details or references please see the help page of the respective
  function.

## Note

The vector of market shares should be in a decimal form corresponding to
total shares of individual firms/units. The vector should sum up to 1.
Alternatively, the user might use
[`concstats_shares()`](https://docs.ropensci.org/concstats/reference/concstats_shares.md)
to converting raw variables, e.g. loans or sales into shares.

## See also

[`concstats_concstats()`](https://docs.ropensci.org/concstats/reference/concstats_concstats.md),
[`concstats_mstruct()`](https://docs.ropensci.org/concstats/reference/concstats_mstruct.md),
[`concstats_inequ()`](https://docs.ropensci.org/concstats/reference/concstats_inequ.md)

Other Competition/Concentration measures:
[`concstats_all_comp()`](https://docs.ropensci.org/concstats/reference/concstats_all_comp.md),
[`concstats_dom()`](https://docs.ropensci.org/concstats/reference/concstats_dom.md),
[`concstats_hhi()`](https://docs.ropensci.org/concstats/reference/concstats_hhi.md),
[`concstats_hhi_d()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_d.md),
[`concstats_hhi_min()`](https://docs.ropensci.org/concstats/reference/concstats_hhi_min.md),
[`concstats_sten()`](https://docs.ropensci.org/concstats/reference/concstats_sten.md)

## Examples

``` r
# a vector of market shares
x <- c(0.35, 0.4, 0.05, 0.1, 0.06, 0.04)

# the Herfindahl-Hirschman index of the vector
concstats_comp(x, type = "hhi")
#> [1] 0.3002

# individual measure
concstats_sten(x)
#> [1] 48.125

# complete group measures
concstats_comp(x, type = "all", digits = 2)
#>        Measure Value
#> 1          HHI  0.30
#> 2     HHI(min)  0.17
#> 3    HHI(dual)  0.44
#> 4    Dominance  0.45
#> 5 Stenbacka(%) 48.12
```
