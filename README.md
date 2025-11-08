# OpenRailFiction
OpenRailFiction is a railway map for OpenGeoFiction, similar to [OpenRailwayMap](openrailwaymap.org)
## How to Use
### Prerequisites
- Have [Python](https://www.python.org/downloads/) installed
- Have a browser

### Instructions

1. Download
2. Unzip into folder
3. Open [Overpass Turbo](https://overpass.opengeofiction.net)
4. Paste

        [out:json][timeout:60];
        area["ogf:id"="Territory"]->.a;
        (
        way["railway"](area.a);
        );
        out body;
        >;
        out skel qt;

    into the text box, and replace Territory with your territory ID
5. Click run, and wait a bit for everything to appear on the map. 
6. On the top bar, click export, then GeoJSON Download.  
7. Name it ```Railways.geojson```, and place in same folder as index.html
8. Run ```run.bat```
9. Open ```Localhost:8000``` in your browser  
