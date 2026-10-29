# Get information about a single occurrence record

Returns information about a single occurrence record from the
Paleobiology Database.

## Usage

``` r
pbdb_occurrence(id, ...)
```

## Arguments

- id:

  Identifier of the occurrence. This parameter is required.

- ...:

  Arguments passed to the API. See all available arguments at
  <https://paleobiodb.org/data1.2/occs/single>. E.g.:

  - `vocab`: Set to `"pbdb"` to show the complete name of the variables
    (by default variables have short 3-letter names).

  - `show`: Select additional blocks of information to be returned along
    with the basic record. Some possible values include:

    - `"class"`: The taxonomic classification of the occurence: phylum,
      class, order, family, genus.

    - `"coords"`: The latitude and longitude of this occurrence.

    - `"loc"`: Additional information about the geographic locality of
      the occurrence

    - `"stratext"`: Detailed information about the stratigraphic context
      of the occurrence.

    - `"lithext"`: Detailed information about the lithological context
      of the occurrence.

## Value

A data frame with a single occurrence.

## Details

Documentation for all the parameters is available at
<https://paleobiodb.org/data1.2/occs/single>. In the parameter list
above, we describe the most common filters that paleontologists and
ecologists might use.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_occurrence(id = 1001)
  pbdb_occurrence(id = 1001, vocab = "pbdb", show = c("class", "coords"))
} # }
```
