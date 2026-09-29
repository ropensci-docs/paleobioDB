# Get information about a single taxonomic opinion

Returns information about a single taxonomic opinion, selected by
identifier.

## Usage

``` r
pbdb_opinion(id, ...)
```

## Arguments

- id:

  Identifier of the opinion. This parameter is required.

- ...:

  Arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/opinions/single>. E.g.:

  - `vocab`: Set to `"pbdb"` to show the complete name of the variables
    (by default variables have short 3-letter names).

  - `show`: Additional information to be shown along with the basic
    record. Some possible values include:

    - `basis`: The basis of the opinion, which can be "stated with
      evidence", "stated without evidence", "implied", or "second hand".

    - `entname`: The names of the people who authorized, entered and
      modified this record.

    - `refattr`: The author(s) and year of publication of the reference
      from which the opinion was entered.

## Value

A data frame with a single taxonomic opinion.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_opinion(id = 1000, vocab = "pbdb", show = "full")
} # }
```
