# Get information about multiple intervals

Returns information about multiple intervals, selected according to the
parameters you provide.

## Usage

``` r
pbdb_intervals(...)
```

## Arguments

- ...:

  arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/intervals/list>. E.g.:

  - `min_ma`: Return only intervals that are at least this old.

  - `max_ma`: Return only intervals that are at most this old.

  - `order`: Return the intervals in order starting as specified.
    Possible values include `"age"`, `"name"`. Defaults to `"age"`.

  - `vocab`: Set to `"pbdb"` to show the complete name of the variables
    (by default variables have short 3-letter names).

## Value

A data frame with information from several temporal intervals.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_intervals(min_ma = 0, max_ma = 2, vocab = "pbdb")
} # }
```
