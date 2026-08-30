# Temporal variation in taxon richness

Returns a data frame of temporal variation in taxon richness in the
indicated temporal extent and resolution from the provided occurrence
data and optionally produces a plot from it.

## Usage

``` r
pbdb_richness(
  data,
  rank = c("species", "genus", "family", "order", "class", "phylum"),
  res = 1,
  temporal_extent = c(0, 10),
  colour = "#0000FF30",
  bord = "#0000FF",
  ylab = "Richness",
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

- res:

  Numeric. Sets the duration of the intervals in the temporal extent.

- temporal_extent:

  Numeric vector to set the temporal extent (min, max).

- colour:

  Colour of the area of the polygon in the plot.

- bord:

  Colour of the border of the polygon.

- ylab:

  A label for the y axis.

- do_plot:

  Logical indicating whether to produce a plot (`TRUE` by default).

## Value

A data frame with the richness aggregated by the taxon rank in the
specified temporal extent and resolution.

## Examples

``` r
if (FALSE) { # \dontrun{
  data <- pbdb_occurrences(
    limit = "all",
    vocab = "pbdb",
    base_name = "Canidae",
    show = "class"
  )
  pbdb_richness(data, rank = "species", res = 0.2, temporal_extent = c(0, 3))
} # }
```
