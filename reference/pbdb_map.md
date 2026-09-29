# Map the fossil records

The function opens a new window with a map showing the distribution of
the fossil records as points. These points are coloured according to the
number of occurrences per cell.

## Usage

``` r
pbdb_map(
  data,
  col_int = "white",
  pch = 19,
  col_ocean = "black",
  main = NULL,
  col_point = c("light blue", "blue"),
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

- col_int:

  The colour of the mainland.

- pch:

  See [`par()`](https://rdrr.io/r/graphics/par.html).

- col_ocean:

  The colour of the ocean.

- main:

  Title of the map. See [`par()`](https://rdrr.io/r/graphics/par.html).

- col_point:

  Two or more colours that are used to generate the colour gradient
  showing the number of occurrences per coordinate in the map.

- do_plot:

  Logical. If `TRUE`, the function produces a plot in addition to
  returning a data frame with the occurrence counts.

- ...:

  Other parameters. See [`par()`](https://rdrr.io/r/graphics/par.html)
  and [`maps::map()`](https://rdrr.io/pkg/maps/man/map.html).

## Value

A data frame with the number of occurrences per coordinate.

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
[`colors()`](https://rdrr.io/r/grDevices/colors.html) help pages.

## Examples

``` r
if (FALSE) { # \dontrun{
  data <- pbdb_occurrences(
    limit = "all", vocab = "pbdb", base_name = "Canis", show = "coords"
  )
  X11(width = 12, height = 8)
  pbdb_map(data)
  pbdb_map(data, pch = 1)
  pbdb_map(
    data,
    pch = 19,
    col_point = c("pink", "red"),
    col_ocean = "light blue",
    main = "Canis"
  )
} # }
```
