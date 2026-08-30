# Plot a raster showing the number of fossil occurrences

Creates a `SpatRaster` object and a plot of the sampling effort (number
of fossil records per cell).

## Usage

``` r
pbdb_map_occur(
  data,
  res = 5,
  col_int = "white",
  col_ocean = "black",
  col_eff = c("light blue", "blue"),
  do_plot = TRUE,
  ...
)
```

## Arguments

- data:

  Input data frame. This data frame is the output of the
  [`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md)
  function using the argument `show = "coords"`. See also Details and
  Examples.

- res:

  The resolution of the `SpatRaster` object (in decimal degrees). See
  [`terra::res()`](https://rspatial.github.io/terra/reference/dimensions.html).

- col_int:

  The colour of the mainland.

- col_ocean:

  The colour of the ocean.

- col_eff:

  Two or more colours that are used to generate the colour gradient
  showing the number of occurrences per cell in the map.

- do_plot:

  Logical. If `TRUE`, the function produces a plot in addition to
  returning a `SpatRaster`.

- ...:

  Other parameters. See [`par()`](https://rdrr.io/r/graphics/par.html)
  and [`maps::map()`](https://rdrr.io/pkg/maps/man/map.html)

## Value

A `SpatRaster` object with the sampling effort (number of fossil records
per cell). This `SpatRaster` object has the resolution that was
specified in the `res` argument. The default is `res = 5`. Users that
wish to work with objects of this type should load package `terra`.

## Details

The argument `show = "coords"` in the
[`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md)
function is required. We recommend the use of a cairo device
([`X11()`](https://rdrr.io/r/grDevices/x11.html)) for better
visualization of the maps. See Examples.

## See also

See
[`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md),
[`maps::map()`](https://rdrr.io/pkg/maps/man/map.html),
[`par()`](https://rdrr.io/r/graphics/par.html) and
[`colors()`](https://rdrr.io/r/grDevices/colors.html) help pages

## Examples

``` r
if (FALSE) { # \dontrun{
  data <- pbdb_occurrences(
    limit = "all", vocab = "pbdb", base_name = "Canis", show = "coords"
  )
  X11(width = 13, height = 7.8)
  pbdb_map_occur(data, res = 2)
  ## Get the raster object without plotting it
  pbdb_map_occur(data, res = 3, do_plot = FALSE)
} # }
```
