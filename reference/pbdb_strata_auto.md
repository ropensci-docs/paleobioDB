# Get a list of strata matching a given prefix or partial name

Returns a list of strata matching the given prefix or partial name. This
can be used to implement auto-completion for strata names, and can be
limited by geographic location if desired.

## Usage

``` r
pbdb_strata_auto(...)
```

## Arguments

- ...:

  Arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/strata/auto>. E.g.:

  - `name`: A full or partial name. It must have at least 3 significant
    characters, and may end in a space followed by either 'g' or 'f' to
    indicate that you are looking for a group or formation.

  - `rank`: Return only strata of the specified rank: `"formation"` or
    `"group"`. This may be overridden by a suffix on the value of
    `name`.

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

  - `vocab`: Set to `"pbdb"` to show the complete name of the variables
    (by default variables have short 3-letter names).

## Value

A data frame with information from the strata that match the `name`
parameter.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_strata_auto(name = "Pin", vocab = "pbdb")
} # }
```
