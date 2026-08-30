# Get references associated with fossil occurrences

Returns information about the bibliographic references associated with
fossil occurrences from the database.

## Usage

``` r
pbdb_ref_occurrences(...)
```

## Arguments

- ...:

  arguments passed to the API. See all available arguments at
  <https://paleobiodb.org/data1.2/occs/refs>

  - `ref_author`: Select only references for which any of the authors
    matches the specified name.

  - `ref_pubyr`: Select only references published in the specified year.

  - `pub_title`: Select only references that involve the specified
    publication.

## Value

A data frame with the information about the references that match the
query.

## Details

Go to
[`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md)
to see an explanation about the main filtering parameters.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_ref_occurrences(vocab = "pbdb", base_name = "Canis", ref_pubyr = 2000)
} # }
```
