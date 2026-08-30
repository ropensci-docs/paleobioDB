# Get a list of taxonomic names matching a prefix or partial name

Returns a list of taxonomic names matching the given prefix or partial
name.

## Usage

``` r
pbdb_taxa_auto(...)
```

## Arguments

- ...:

  Arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/taxa/auto>. E.g.:

  - `name`: A partial name or prefix. It must have at least 3
    significant characters, and may include both a genus (possibly
    abbreviated) and a species.

  - `limit`: Set the limit to the number of matches.

## Value

A data frame with information about the matches (taxon rank and number
of occurrences in the database).

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_taxa_auto(name = "Cani", limit = 10)
} # }
```
