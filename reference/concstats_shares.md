# shares

The `concstats_shares` function is a helper function making it easier to
convert numeric variable into individual shares. This might be
convenient for larger vectors.

## Usage

``` r
concstats_shares(x, na.rm = TRUE, digits = NULL)
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

A numeric vector in decimal form.

## Details

`concstats_shares` is a helper function. The user can manually convert
or provide numerical vectors of shares or use `constats_shares`.

## Examples

``` r
# a vector of loans (without special characters, e.g. currency symbols)
x <- c(538572286.08, 481096.77, 161914143.03, 128796268.59, 69055940.72)
concstats_shares(x)
#> [1] 0.5991994446 0.0005352539 0.1801408410 0.1432948828 0.0768295777

# a vector with NA values
x2 <- c(538572286.08, 481096.77, 161914143.03, 128796268.59, 69055940.72, NA)
concstats_shares(x2, na.rm = TRUE, digits = 3)
#> `x` has NA values. NAs have been removed for computation.
#> [1] 0.599 0.001 0.180 0.143 0.077
```
