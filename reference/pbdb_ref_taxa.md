# Get references for taxonomic names

Returns information about the source references associated with taxa in
the Paleobiology Database. You can use the same parameters that are
available with `pbdb_taxa`, but reference records are returned instead
of taxon records. One record is returned per reference, even if it is
associated with multiple taxa.

## Usage

``` r
pbdb_ref_taxa(...)
```

## Arguments

- ...:

  Arguments passed to the API. See all available arguments at
  <https://paleobiodb.org/data1.2/taxa/refs>

  - `name`: Returns information about the most fundamental taxonomic
    name matching this string. The % and \_ characters may be used as
    wildcards.

  - `id`: Returns information about the taxonomic name corresponding to
    this identifier. You may not specify both `name` and `id` in the
    same query.

  - `show`: Show extra variables.

  - `rel`: Set `rel = "synonyms"` to select all synonyms of the base
    taxon or taxa; `rel = "children"` to select the taxa immediately
    contained within the base taxon or taxa; `rel = "all_children"` to
    select all taxa contained within each matching taxon and within all
    synonymous taxa; `rel = "all_parents"` to select all taxa that
    contain any of the matching taxa.

  - `extant`: Logical indicating whether to select only extant or
    non-extant taxa.

## Value

A data frame with references from a list of taxa.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_ref_taxa(
    name = "Canidae", vocab = "pbdb", show = c("both", "comments")
  )
} # }
```
