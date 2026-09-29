# Get information about a single interval

Returns information about a single interval, selected by identifier.

## Usage

``` r
pbdb_interval(...)
```

## Arguments

- ...:

  Additional arguments passed to the API. See documentation for accepted
  parameters at <https://paleobiodb.org/data1.2/intervals/single>.
  Either `name` or `id` must be specified, but both cannot be used in
  the same query:

  - `name`: Returns the interval with the specified name.

  - `id`: Returns the interval corresponding to the specified
    identifier.

  - `vocab`: Set to `"pbdb"` to show the complete name of the variables
    (by default variables have short 3-letter names).

## Value

A data frame with information from a single temporal interval.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_interval(id = 1, vocab = "pbdb")
} # }
```
