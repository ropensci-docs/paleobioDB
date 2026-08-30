# Temporal range of taxa

Returns a data frame with the temporal range of the taxa within a
selected rank (species, genera, families, etc.), and optionally
generates a plot from it.

## Usage

``` r
pbdb_temp_range(
  data,
  rank = c("species", "genus", "family", "order", "class", "phylum"),
  col = "#0000FF",
  names = TRUE,
  do_plot = TRUE
)
```

## Arguments

- data:

  Data frame from a query to PaleobioDB as returned by
  [`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md).
  Important: it is required to have information about the taxonomic
  classification of the occurrences in the data frame, to do that set
  the `show` parameter to `"class"` or `"classext"` (see Examples).

- rank:

  The taxon rank to be analyzed. The default value is `"species"`.

- col:

  Colour of the bars in the plot.

- names:

  Logical indicating whether to include the name of the taxa in the plot
  (`TRUE` by default).

- do_plot:

  Logical value indicating whether to produce a plot (`TRUE` by
  default).

## Value

A data frame with the time span of the taxa selected (species, genera,
etc.).

## Examples

``` r
if (FALSE) { # \dontrun{
  canis_quaternary <- pbdb_occurrences(
    limit = "all", base_name = "Canis", interval = "Quaternary",
    show = c("coords", "classext"), vocab = "pbdb"
  )
  pbdb_temp_range(canis_quaternary, rank = "species", names = FALSE)
} # }
```
