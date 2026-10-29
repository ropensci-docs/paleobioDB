# Temporal resolution of fossil data

Shows the temporal resolution of the fossil data.

## Usage

``` r
pbdb_temporal_resolution(data, do_plot = TRUE)
```

## Arguments

- data:

  Data frame from a query to PaleobioDB as returned by
  [`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md).

- do_plot:

  Logical. If `TRUE`, the function creates a frequency plot of the data.

## Value

A list with a summary of the temporal resolution of the data (min, max,
1st and 3rd quartiles, median and mean), and the temporal resolution of
each fossil record (Ma).

## Examples

``` r
if (FALSE) { # \dontrun{
  data <- pbdb_occurrences(taxon_name = "Canidae", interval = "Quaternary")
  pbdb_temporal_resolution(data)
} # }
```
