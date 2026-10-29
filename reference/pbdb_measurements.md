# Get information about specimen measurements

Returns information about the measurements associated with the selected
fossil specimens.

## Usage

``` r
pbdb_measurements(...)
```

## Arguments

- ...:

  Arguments passed to the API. See all available arguments at
  <https://paleobiodb.org/data1.2/specs/measurements>.

  The following parameters can be used to retrieve measurements from a
  known list of specimens, occurrences, or collections. Only the records
  matching all specified parameters will be returned:

  - `spec_id`: A list of specimen identifiers.

  - `occ_id`: A list of occurrence identifiers.

  - `coll_id`: A list of collection identifiers.

  It is possible to return additional information along with the basic
  record with the following parameter:

  - `show`: Possible values include:

    - `"spec"`: Includes all of the core fields describing the specimen
      from which this measurement was taken.

    - `"methods"`: Information about the collection methods used.

  See the
  [`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md)
  documentation for an explanation about more filtering parameters.

## Value

A data frame with information about the measurements that match the
query.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_measurements(
    spec_id = c(1505, 30050),
    show = c("spec", "class", "methods"),
    vocab = "pbdb"
  )
} # }
```
