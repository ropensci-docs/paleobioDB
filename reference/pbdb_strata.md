# Get information about geological strata

Returns information about geological strata, selected by name, rank,
and/or geographic location.

## Usage

``` r
pbdb_strata(...)
```

## Arguments

- ...:

  Arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/strata/list>. E.g.:

  - `name`: A full or partial name. You can use % and \_ as wildcards.

  - `rank`: Returns only strata of the specified rank: `"formation"`,
    `"group"` or `"member"`.

  - `lngmin`: Numeric. The longitude boundaries will be normalized to
    fall between -180 and 180. Note that if you specify `lngmin` then
    you must also specify `lngmax`. Returns only records whose
    geographic location falls within the given bounding box (defined by
    `lngmin`, `lngmax`, `latmin`, `latmax`). It generates two adjacent
    bounding boxes if the range crosses the antimeridian.

  - `lngmax`: Numeric. The longitude boundaries will be normalized to
    fall between -180 and 180.

  - `latmin`: Numeric between -90 and 90. Note that if you specify
    `latmin` then you must also specify `latmax`.

  - `latmax`: Numeric between -90 and 90.

  - `loc`: Return only strata associated with some occurrence whose
    geographic location falls within the specified geometry, specified
    in WKT format.

  - `vocab`: Set to `"pbdb"` to show the complete name of the variables
    (by default variables have short 3-letter names).

## Value

A data frame with information from the selected strata.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_strata(
    lngmin = 0, lngmax = 15, latmin = 0, latmax = 15,
    rank = "formation", vocab = "pbdb"
  )
} # }
```
