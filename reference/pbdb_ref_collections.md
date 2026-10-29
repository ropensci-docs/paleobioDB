# Get references from which collection data were entered

Returns information about the references from which the selected
collection data were entered.

## Usage

``` r
pbdb_ref_collections(...)
```

## Arguments

- ...:

  Arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/colls/refs>. E.g.:

  - `coll_id`: List of collection identifiers.

  - `ref_author`: Select only references for which any of the authors
    matches the specified name.

  - `ref_pubyr`: Select only references published in the specified year.

  - `pub_title`: Select only references that involve the specified
    publication.

  - `order`: Specifies the order in which the results are returned. You
    can specify multiple values separated by commas, and each value may
    be appended with .asc or .desc. Accepted values are: `"author"`,
    `"pubyr"`, `"reftitle"`, `"pubtitle"`, `"pubtype"`, `"created"`,
    `"modified"`, `"rank"`.

## Value

A data frame with the information about the references that match the
query.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_ref_collections(
    base_name = "Canidae",
    interval = "Quaternary",
    cc = "ASI"
  )
} # }
```
