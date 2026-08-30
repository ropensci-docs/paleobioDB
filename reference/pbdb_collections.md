# Get information about multiple collections

Returns information about multiple collections, selected according to
the parameters you provide.

## Usage

``` r
pbdb_collections(...)
```

## Arguments

- ...:

  Additional arguments passed to the API. See all available arguments at
  <https://paleobiodb.org/data1.2/colls/list>. Go to
  [`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md)
  to see an explanation about the main filtering parameters.

## Value

A data frame with the collections that match the query.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_collections(base_name = "Cetacea", interval = "Miocene")
} # }
```
