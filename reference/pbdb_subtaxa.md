# Count number of taxa in an occurrence data frame

Count the number of taxa (species, genera, families, orders, classes,
and phyla) in an occurrence data frame.

## Usage

``` r
pbdb_subtaxa(data, do_plot = TRUE, col = "#0000FF")
```

## Arguments

- data:

  Data frame from a query to PaleobioDB as returned by the
  [`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md)
  function using the argument `show = "class"` or `show = "classext"`.

- do_plot:

  Logical indicating whether to produce a plot (`TRUE` by default).

- col:

  Colour of the histogram.

## Value

A data frame with the number of subtaxa in the data.

## Examples

``` r
if (FALSE) { # \dontrun{
  canidae_quat <- pbdb_occurrences(
    limit = "all", base_name = "Canidae",  interval = "Quaternary",
    show = c("coords", "classext", "ident"), vocab = "pbdb"
  )
  pbdb_subtaxa(canidae_quat)
} # }
```
