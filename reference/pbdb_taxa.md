# Get information about multiple taxonomic names

Returns information about multiple taxonomic names. This function can be
used to query for all of the children or parents of a given taxon, among
other operations.

## Usage

``` r
pbdb_taxa(...)
```

## Arguments

- ...:

  Arguments passed to the API. See all available arguments at
  <https://paleobiodb.org/data1.2/taxa/list>.

  - `name`: Returns information about the most fundamental taxonomic
    name matching this string. The % and \_ characters may be used as
    wildcards.

  - `id`: Return information about the taxonomic name corresponding to
    this identifier. You may not specify both `name` and `id` in the
    same query.

  - `show`: Show extra variables. Some examples include: `"attr"` the
    attribution of this taxon (author and year); `"app"` the age of
    first and last appearance of this taxon from the occurrences
    recorded in this database; `"size"` the number of subtaxa appearing
    in this database.

  - `rel`: Set `rel = "synonyms"` to select all synonyms of the base
    taxon or taxa; `rel = "children"` to select the taxa immediately
    contained within the base taxon or taxa; `rel = "common"` to select
    the most specific taxon that contains all of the base taxa.

  - `extant`: Logical indicating whether to select only extant or
    non-extant taxa.

## Value

A data frame with information from a list of taxa.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_taxa(name = "Canidae", rel = "all_parents", vocab = "pbdb",
            show = c("attr", "app", "size", "class"))
  pbdb_taxa(id = c(10, 11), vocab = "pbdb",
            show = c("attr", "app", "size", "class"))
  pbdb_taxa(
    id = c(10, 11), vocab = "pbdb",
    show = c("attr", "app", "size", "class"), rel = "common"
  )
} # }
```
