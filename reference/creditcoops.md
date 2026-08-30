# Creditcoops

data set with 22 paired Paraguayan credit cooperatives (2016, 2018)

## Usage

``` r
data(creditcoops)
```

## Format

A data frame with 44 rows and 5 variables:

- `coop_id`:

  double, ID of the credit cooperative

- `year`:

  integer, sample year

- `total_loans`:

  double, total loans granted (USD) per year and cooperative

- `paired`:

  integer, paires of cooperatives

- `total_loans_log`:

  double, the natural log of total loans

## Source

<http://www.incoop.gov.py/v2/>

## Note

real names of the cooperatives have been purposely omitted, but are
available on request.

## Author

Andreas Schneider

## Examples

``` r
data("creditcoops")
head(creditcoops)
#> # A tibble: 6 × 5
#>   coop_id year  total_loans paired total_loans_log
#>     <dbl> <fct>       <dbl>  <int>           <dbl>
#> 1       1 2016    173892358      1            19.0
#> 2       1 2018    199048199      1            19.1
#> 3       2 2016    323892456      2            19.6
#> 4       2 2018    461609439      2            20.0
#> 5       3 2016    179981404      3            19.0
#> 6       3 2018    227232008      3            19.2
```
