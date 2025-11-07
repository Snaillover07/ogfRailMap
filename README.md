# Opengeofiction Railway Map
Opengeofiction Railway Map is a railway map for OpenGeoFiction, similar to [OpenRailwayMap](openrailwaymap.org)
## How to Use
### Prerequisites
- Have [Python](https://www.python.org/downloads/) installed
- Have a brower

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
5. Replace Territory with your territory ID, then click run  
6. On the top bar, click export, then GeoJSON Download.  
7. Name it ```Railways.geojson```, and place in same folder as index.html  
8. Open command prompt / terminal, and type in ```cd "Your folder path"```  
9. Run ```python3 -m http.server 8000```  
10. Open ```Localhost:8000``` in your browser  
