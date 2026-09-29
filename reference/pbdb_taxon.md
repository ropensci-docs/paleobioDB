# Get information about a single taxonomic name

Returns information about a single taxonomic name, identified either by
name or by identifier.

## Usage

``` r
pbdb_taxon(...)
```

## Arguments

- ...:

  Arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/taxa/single>. One of the following
  parameters must be specified (but not both):

  - `name`: Returns information about the most fundamental taxonomic
    name matching this string. The % and \_ characters may be used as
    wildcards.

  - `id`: Returns information about the taxonomic name corresponding to
    the specified identifier. The value can have different forms (see
    the API documentation in the link above).

## Value

A data frame with information from a single taxon.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_taxon(name = "Canis", vocab = "pbdb",
             show = c("attr", "app", "size"))
} # }
```
