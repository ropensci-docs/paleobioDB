# Get information about geographic clusters of collections

This path returns information about geographic clusters of collections
from the Paleobiology Database. These clusters are defined in order to
facilitate the generation of maps at low resolutions. You can make a
config request via <https://paleobiodb.org/data1.2/config> in order to
get a list of the available summary levels.

## Usage

``` r
pbdb_collections_geo(level, ...)
```

## Arguments

- level:

  An integer specifying a cluster level. Refer to
  <https://paleobiodb.org/data1.2/config.txt?show=clusters> for a list
  of available resolution levels ("cluster_level" column).

- ...:

  Documentation for all the parameters is available at
  <https://paleobiodb.org/data1.2/colls/summary>. Go to
  [`pbdb_occurrences()`](https://docs.ropensci.org/paleobioDB/reference/pbdb_occurrences.md)
  to see an explanation about the main filtering parameters.

## Value

A data frame with the collections that match the query.

## Examples

``` r
if (FALSE) { # \dontrun{
  pbdb_collections_geo(
    level = 2,
    vocab = "pbdb",
    lngmin = 0.0, lngmax = 15.0, latmin = 0.0, latmax = 15.0
  )
} # }
```
