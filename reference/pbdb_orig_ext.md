# Appearance of new taxa and extinctions across time

Returns a data frame with the appearance of new taxa and their last
appearances across time in the provided data and optionally produces a
plot from it, showing the new appearances or last appearances.

## Usage

``` r
pbdb_orig_ext(
  data,
  rank = c("species", "genus", "family", "order", "class", "phylum"),
  temporal_extent,
  res,
  orig_ext = 1,
  colour = "#0000FF30",
  bord = "#0000FF",
  ylab = NULL,
  do_plot = TRUE
)
```

## Arguments

- data:

  Data frame from a query to PaleobioDB as returned by
  [`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md).
  Important: it is required to show the name of the families, orders,
  etc. in the data frame, to do that set:
  `show = c("classext", "ident")` (see Examples).

- rank:

  The taxon rank to be analyzed. Its default value is `"species"`.

- temporal_extent:

  Vector to set the temporal extent (min, max)

- res:

  Numeric. Sets the intervals of the temporal extent.

- orig_ext:

  Set to 1 to plot the number new appearances, or to 2 to plot the
  number of extinctions.

- colour:

  Colour of the area of the polygon in the plot.

- bord:

  Colour of the border of the polygon.

- ylab:

  A label for the y axis.

- do_plot:

  Logical value indicating whether to produce a plot (`TRUE` by
  default).

## Value

A data frame with the number of first appearances and extinctions of the
selected taxon rank across time.

## Examples

``` r
if (FALSE) { # \dontrun{
  canidae <- pbdb_occurrences(
    limit = "all", vocab = "pbdb",
    base_name = "Canidae", show = "classext"
  )

  # Plot of the evolutionary rates
  pbdb_orig_ext(
    canidae,
    rank = "genus",
    orig_ext = 1,
    temporal_extent = c(0, 10), res = 1
  )

  # Plot of the extinction rates
  pbdb_orig_ext(
    canidae,
    rank = "genus",
    orig_ext = 2,
    temporal_extent = c(0, 10), res = 1
  )
} # }
```
