# Plot a raster showing the richness of taxa

Creates a `SpatRaster` object and a plot with richness of species,
genera, families, etc. per cell.

## Usage

``` r
pbdb_map_richness(
  data,
  rank = c("species", "genus", "family", "order", "class", "phylum"),
  do_plot = TRUE,
  res = 5,
  col_int = "white",
  col_ocean = "black",
  col_rich = c("light blue", "blue"),
  title = "Taxonomic richness",
  ...
)
```

## Arguments

- data:

  Input data frame. This data frame is the output of the
  [`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md)
  function using the argument `show = c("coords", "classext")`. See also
  Details and Examples.

- rank:

  Taxon rank for which richness is calculated. The options are:
  `"species"`, `"genus"`, `"family"`, `"order"`, `"class"` or
  `"phylum"`. The default value is `"species"`.

- do_plot:

  Logical. If `TRUE`, the function produces a plot in addition to
  returning a `SpatRaster`.

- res:

  The resolution of the `SpatRaster` object (in decimal degrees). See
  [`terra::res()`](https://rspatial.github.io/terra/reference/dimensions.html).

- col_int:

  The colour of the mainland.

- col_ocean:

  The colour of the ocean.

- col_rich:

  Two or more colours that are used to generate the colour gradient
  showing the richness per cell in the map.

- title:

  A title for the plot, to be positioned to the right of the legend.

- ...:

  Other parameters. See [`par()`](https://rdrr.io/r/graphics/par.html)
  and [`maps::map()`](https://rdrr.io/pkg/maps/man/map.html).

## Value

A `SpatRaster` object with the richness of the specified taxon rank per
cell. This `SpatRaster` object has the resolution that was specified in
the `res` argument. The default is `res = 5`. Users that wish to work
with objects of this type should load package `terra`.

## Details

The argument `show = c("coords", "classext")` in the
[`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md)
function is required. We recommend the use of a cairo device
([`X11()`](https://rdrr.io/r/grDevices/x11.html)) for better
visualization of the graphs. See Examples.

## See also

See
[`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md),
[`maps::map()`](https://rdrr.io/pkg/maps/man/map.html),
[`par()`](https://rdrr.io/r/graphics/par.html) and
[`colors()`](https://rdrr.io/r/grDevices/colors.html) help pages.

## Examples

``` r
if (FALSE) { # \dontrun{
  data <- pbdb_occurrences(
    limit = 1000, vocab = "pbdb", base_name = "mammalia",
    show = c("classext", "coords")
  )
  X11(width = 13, height = 7.8)
  pbdb_map_richness(data, res = 8, rank = "genus")
  pbdb_map_richness(data, res = 8, rank = "family")
  ## Get the raster object without plotting the map
  pbdb_map_richness(data, res = 8, rank = "family", do_plot = FALSE)
} # }
```
