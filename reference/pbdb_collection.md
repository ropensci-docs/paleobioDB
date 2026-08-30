# Get information about a single collection record

Returns information about a single collection record from the
Paleobiology Database.

## Usage

``` r
pbdb_collection(id, ...)
```

## Arguments

- id:

  Identifier of the collection. This parameter is required.

- ...:

  Additional arguments passed to the API. See all available arguments at
  <https://paleobiodb.org/data1.2/colls/single>. E.g.:

  - `vocab`: Set to "pbdb" to show the complete name of the variables
    (by default variables have short 3-letter names).

  - `show`: Select additional blocks of information to be returned along
    with the basic record. Some possible values include:

    - `"loc"`: Additional information about the geographic locality of
      the collection

    - `"stratext"`: Detailed information about the stratigraphic context
      of collection.

    - `"lithext"`: Detailed information about the lithological context
      of the collection.

## Value

A data frame with a single occurrence.

## Details

Go to
[`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md)
to see an explanation about the main parameters.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_collection(id = 1003, vocab = "pbdb", show = c("loc", "stratext"))
} # }
```
