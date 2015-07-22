# Leaflet.Shapefile.js

Shapefiles in Leaflet. Taking the Leaflet.draw plugin to the next level,
Leaflet.Shapefile is a plugin for uploading and downloading shapefiles
in a Leaflet map. Leaflet.Shapefile.js uses Shapefile.io endpoints
[/upload](http://docs.shapefile.io/docs/upload), [/new](http://docs.shapefile.io/docs/new-1)
and [/download](http://docs.shapefile.io/docs/download) to handle uploads and downloads.

### Uploading

Just like [Leaflet.draw](https://github.com/Leaflet/Leaflet.draw) enables
features to be drawn in a [FeatureGroup](http://leafletjs.com/reference.html#featuregroup),
Leaflet.Shapefile uploads allows a user to upload a shapefile's features to a
[FeatureGroup](http://leafletjs.com/reference.html#featuregroup).
Feature responses are projected to WGS84.

### Downloading

Download a [FeatureGroup](http://leafletjs.com/reference.html#featuregroup) as a shapefile.
Note that all features in the FeatureGroup must be of the same type: Points, Polylines, Polygons, etc.

### Usage

```
var controlOptions = {
  draw: false,
  shapefile: {
    featureGroup: drawnItems,
      upload: true,
      download: true
  }
}

drawControl = new L.Control.Draw(controlOptions).addTo(map);
```
