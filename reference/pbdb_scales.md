# Get information about multiple time scales

Returns information about multiple time scales.

## Usage

``` r
pbdb_scales(...)
```

## Arguments

- ...:

  Arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/timescales/list>. E.g.:

  - `all_records`: Set to `TRUE` to list all intervals.

  - `id`: Return only time scales with the specified identifier(s). It
    is possible to provide multiple identifiers as a comma-separated
    list.

  - `name`: Return only time scales with the specified name(s). It is
    possible to provide multiple names as a comma-separated list.

  - `vocab`: Set to `"pbdb"` to show the complete name of the variables
    (by default variables have short 3-letter names).

## Value

A data frame with information from the selected scales.

## Examples

``` r
if (FALSE) { # \dontrun{
  ## Get a data frame with all the scales available in PBDB
  ## by setting no ids
  pbdb_scales(all_records = TRUE)
} # }
```
