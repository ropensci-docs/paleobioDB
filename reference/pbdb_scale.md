# Get information about a single time scale

Returns information about a single time scale, selected by identifier.

## Usage

``` r
pbdb_scale(id, ...)
```

## Arguments

- id:

  Identifier of the temporal interval. This parameter is required.

- ...:

  Additional arguments passed to the API. See documentation for accepted
  parameters at <https://paleobiodb.org/data1.2/timescales/single>.
  E.g.:

  - `vocab`: Set to `"pbdb"` to show the complete name of the variables
    (by default variables have short 3-letter names).

## Value

A data frame with information from a single scale.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_scale(id = 1, vocab = "pbdb")
} # }
```
