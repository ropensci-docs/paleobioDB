# Get information about a single fossil specimen

Returns information about a single fossil specimen, identified either by
name or by identifier.

## Usage

``` r
pbdb_specimen(id, ...)
```

## Arguments

- id:

  The identifier of the specimen. This parameter is required.

- ...:

  Arguments passed to the API. See all available arguments at
  <https://paleobiodb.org/data1.2/specs/single>.

  - `vocab`: Set to "pbdb" to show the complete name of the variables
    (by default variables have short 3-letter names).

  - `show`: Select additional blocks of information to be returned along
    with the basic record. Some possible values include:

    - `"loc"`: Additional information about the geographic locality of
      the associated occurrence, if any.

    - `"stratext"`: Detailed information about the stratigraphic context
      of the associated occurrence.

    - `"lithext"`: Detailed information about the lithological context
      of the associated occurrence.

    - `"refattr"`: The author(s) and year of publication of the
      reference from which this data was entered. If no reference is
      recorded for this specimen, the information from the associated
      occurrence or collection reference is returned instead.

## Value

A data frame with information about a single specimen.

## Examples

``` r
if (FALSE) { # \dontrun{
pbdb_specimen(id = 30050, show = c("class", "loc", "refattr"))
} # }
```
