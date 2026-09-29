# Get information about fossil occurrence records

Returns information about fossil occurrence records stored in the
Paleobiology Database.

## Usage

``` r
pbdb_occurrences(...)
```

## Arguments

- ...:

  Arguments passed to the API. See all available arguments at
  <https://paleobiodb.org/data1.2/occs/list>.

  - `limit`: Limits the number of records returned. The value may be a
    positive integer, zero, or `"all"`.

  - `taxon_name`: Return only records associated with the specified
    taxonomic name(s). You may specify multiple names.

  - `base_name`: Return records associated with the specified taxonomic
    name(s) and any of their children (e.g. `base_name = "Canis"` will
    return "Canis", "Canis lupus", "Canis mosbachensis", etc.)

  - `lngmin`: Numeric. The longitude boundaries will be normalized to
    fall between -180 and 180. Note that if you specify `lngmin` then
    you must also specify `lngmax`. Returns only records whose
    geographic location falls within the given bounding box (defined by
    `lngmin`, `lngmax`, `latmin`, `latmax`). It generates two adjacent
    bounding boxes if the range crosses the antimeridian.

  - `lngmax`: Numeric. The longitude boundaries will be normalized to
    fall between -180 and 180.

  - `latmin`: Numeric value between -90 and 90. Note that if you specify
    `latmin` then you must also specify `latmax`.

  - `latmax`: Numeric value between -90 and 90.

  - `min_ma`: Return only records whose temporal locality is at least
    this old, specified in millions of years.

  - `max_ma`: Return only records whose temporal locality is at most
    this old, specified in millions of years.

  - `interval`: Return only records whose temporal locality falls within
    the named geologic time interval (e.g. "Miocene").

  - `cc`: Return only records whose location falls within the specified
    geographic regions. The value of this parameter should be one or
    more two-character country codes and/or three-character continent
    codes as a comma-separated list (see
    <https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2> and
    <https://paleobiodb.org/data1.2/config.txt?show=continents>). If the
    parameter value starts with !, then records falling into these
    regions are excluded instead of included. Any country codes starting
    with ^ are subtracted from the filter.

  - `show`: Show extra variables (e.g. `"coords"`, `"classext"`,
    `"ident"`).

## Value

A data frame with the fossil occurrences.

## Details

Documentation for all the parameters is available at
<https://paleobiodb.org/data1.2/occs/list>. We describe the most common
filters that paleontologists and ecologists might use in the parameter
list above.

Be aware that depending on the query, some columns may not be returned
by the API if those are empty across all the rows.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_occurrences(id = c(10, 11), show = c("coords", "classext", "ident"))
  pbdb_occurrences(
    limit = "all", vocab = "pbdb", taxon_name = "Canis",
    show = c("coords", "classext", "ident")
  )
  pbdb_occurrences(
    limit = "all", vocab = "pbdb", base_name = "Canidae",
    show = c("coords", "classext", "ident")
  )
} # }
```
