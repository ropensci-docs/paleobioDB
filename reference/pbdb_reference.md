# Get information about a single reference

Returns information about a single reference, selected by identifier.

## Usage

``` r
pbdb_reference(id, ...)
```

## Arguments

- id:

  Identifier of the reference. This parameter is required.

- ...:

  Arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/refs/single>. E.g.:

  - `vocab`: Set to `"pbdb"` to show the complete name of the variables
    (by default variables have short 3-letter names).

  - `show`: Additional information to be shown along with the basic
    record. Some possible values include:

    - `counts`: Report the number of taxonomic names, opinions,
      occurrences, specimens, and collections derived from this
      reference that have been entered into the database.

    - `both`: Show both the formatted reference and the individual
      fields.

## Value

A data frame with a single reference.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_reference(id = 1003, vocab = "pbdb", show = "both")
} # }
```
