# Get references for fossil specimens

Returns information about the bibliographic references associated with
the selected fossil specimens.

## Usage

``` r
pbdb_ref_specimens(...)
```

## Arguments

- ...:

  Arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/specs/refs>. E.g.:

  - `spec_id`: List of specimen identifiers.

  - `base_name`: Return only records associated with the specified
    taxonomic name(s), including all subtaxa and synonyms.

  - `ref_author`: Select only references for which any of the authors
    matches the specified name.

  - `ref_pubyr`: Select only references published in the specified year.

  - `pub_title`: Select only references that involve the specified
    publication.

## Value

A data frame with the information about the references that match the
query.

## Examples

``` r
if (FALSE) { # \dontrun{
pbdb_ref_specimens(spec_id = c(1505, 30050))
} # }
```
