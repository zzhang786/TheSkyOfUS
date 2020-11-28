Visualizes flights between airports in the continental United States using edge bundling. The code can be easily modified to either show the top 50 airports by degree or the highest degree airport in each state.

This example combines our map and graph visualizations together in a single visualization. It demonstrates map projections, TopoJSON, Voronoi diagrams, force-directed layouts, and edge bundling.

## Libraries

The following JavaScript libraries are required for this example:

  - [D3.js](https://d3js.org/)
  - [TopoJSON](https://github.com/topojson/topojson)
  - [us-atlas](https://github.com/topojson/us-atlas)
  - [d3-geo-voronoi](https://github.com/Fil/d3-geo-voronoi)

## Data

This example uses the [`airports.csv`](https://gist.github.com/mbostock/7608400#file-airports-csv) and [`flights.csv`](https://gist.github.com/mbostock/7608400#file-flights-csv) datasets from this GIST:

  - <https://gist.github.com/mbostock/7608400>

The [`airports.csv`](https://gist.github.com/mbostock/7608400#file-airports-csv) file looks like:

| iata | name | city | state | country | latitude | longitude |
|:-----|:-----|:-----|:------|:--------|---------:|----------:|
| 00M | Thigpen | Bay Springs | MS | USA | 31.95376472 | -89.23450472 |
| 00R | Livingston Municipal | Livingston | TX | USA | 30.68586111 | -95.01792778 |

The [`flights.csv`](https://gist.github.com/mbostock/7608400#file-flights-csv) file looks like:

| origin | destination | count |
|:-------|:------------|------:|
| ABE | ATL | 853 |
| ABE | BHM | 1 |

This example also uses the TopJSON data from:

  - <https://github.com/topojson/us-atlas>

The already-projected state-level data is used here.

## Inspirations

The following examples from [Mike Bostock](https://bost.ocks.org/mike/) served as a starting point for the underlying data, map, and interaction:

  - [U.S. Airports Voronoi](https://observablehq.com/@mbostock/u-s-airports-voronoi), an Observable notebook using D3 v5 and TopoJSON v3

  - [Voronoi Arc Map](https://bl.ocks.org/mbostock/7608400), a Block using D3 v4 and TopoJSON v1

  - [Airports Symbol Map](http://mbostock.github.io/d3/talk/20111116/airports.html), a example from a talk using D3 v3

The [Flight Patterns](http://www.aaronkoblin.com/work/flightpatterns/) work by Aaron Koblin and [Force Directed Edge Bundling for Graph Visualization](https://doi.org/10.1111/j.1467-8659.2009.01450.x) paper by [Danny Holten](http://www.win.tue.nl/vis1/home/dholten/#research) and Jarke J. van Wijk are also inspirations for using edge bundling with this example.
