# Get information about multiple references

Returns information about multiple references, selected according to the
parameters you provide.

## Usage

``` r
pbdb_references(...)
```

## Arguments

- ...:

  Arguments passed to the API. See documentation for accepted parameters
  at <https://paleobiodb.org/data1.2/refs/list>. E.g.:

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
  pbdb_references(ref_author = "Polly")
} # }
```
