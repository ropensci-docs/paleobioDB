# Get information about multiple fossil specimens

Returns information about multiple fossil specimens, selected according
to the parameters you provide. Depending upon which output blocks you
select (`show` parameter), the response will contain some fields
describing the specimens and some describing the occurrences and
collections (if any) with which they are associated.

## Usage

``` r
pbdb_specimens(...)
```

## Arguments

- ...:

  Arguments passed to the API. See all available arguments at
  <https://paleobiodb.org/data1.2/specs/list>. See the
  [`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md)
  documentation for an explanation about the main filtering parameters.

## Value

A data frame with the fossil specimens that match the query.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_specimens(base_name = "Cetacea", interval = "Miocene", vocab = "pbdb")
} # }
```
