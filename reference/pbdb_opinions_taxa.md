# Get taxonomic opinions about taxa

Returns information about the taxonomic opinions used to build the
taxonomic hierarchy. From all of the opinions entered into the database
about a particular taxon, the most recent opinion that is stated with
the most evidence is used to classify that taxon. The others are
considered to be superseded and are ignored.

## Usage

``` r
pbdb_opinions_taxa(...)
```

## Arguments

- ...:

  Arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/taxa/opinions>.

## Value

A data frame with information about the taxonomic opinions that match
the query.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_opinions_taxa(base_name = "Canis")
} # }
```
