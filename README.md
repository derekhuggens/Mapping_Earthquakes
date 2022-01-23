# Mapping_Earthquakes
JS &amp; APIs with GeoJSON

### Purpose

#### The purpose of this repository was:

  * Learning source control using `git checkout`, `git checkout -b`, and `git push --set-upstream origin`.
  * Using Leaflet for JS, Mapbox API, and D3.json to create maps with:
    1. `L.tileLayer` for map backgrounds
    2. `baseMaps` base layer to hold multiple map selections such as a street view or satellite view
    3. `new L.LayerGroup()` to hold layer groups that can be turned on and off in `L.control.layers()`
    4. `L.map()` to create a default map object
    5. `L.control.layers()` with `.addTo()` to control which layers are visible
    6. `D3.json().then(function(anonymous) {}` to retrieve GeoJSON data
    7. `L.geoJson(anonymous, {}` to create a GeoJSON layer with retrieved data.
    8. `pointToLayer:`, `style:` Option, and `onEachFeature:` within `L.geoJson` braces to create markers, styling, and feature popups (returning `L.circleMarker` for `pointToLayer:`
    9. `let legend = L.control({
        position: "bottomright"
        });` to create a legend
    10. ` legend.onAdd = function() {
        let div = L.DomUtil.create("div", "info legend");` to add legend details
    11. `div.innerHTML +=
        "<i style='background: " + colors[i] + "'></i> " +
        magnitudes[i] + (magnitudes[i + 1] ? "&ndash;" + magnitudes[i + 1] + "<br>" : "+");` to add colored legend squares (referring to magnitude and color arrays)
