# Data notes for the identification and mapping of cycling routes in Stuttgart with lowest NO2 exposure

## Baden-Würrtemberg Administrative Boundaries
-	Source: https://opengeodata.lgl-bw.de/#/(sidenav:product/alkisvg)
-	Downloaded: 06/09/2026
-	44 Features, polygons, only 1 selected (Stuttgart)
-	Columns in German: Kreis_id (Integer), kreis_name (string), region_id (integer), region_nam (string), regierungs (integer), regierungs_1 (string), beginn (string), ende (string)
-	No nulls in region_nam
-	Covers Stuttgart Fully

  
## Geofabrik (OSM) roads 
-	Source : https://download.geofabrik.de/europe/germany/baden-wuerttemberg/stuttgart-regbez.html
-	Downloaded: 13/09/2026
-	69,163 features, lines
-	Columns: fid (real), osm_id (string), code (integer), fclass (string), name (string), ref (string), oneway (string), maxspeed (integer), layer (integer), bridge (string), tunnel (string)
-	Classified as secondary, residential, tertiary, footway, path, pedestrian, cycleway, and some unclassified in fclass
-	Coverage is detailed across the study area (Stuttgart)

  
## Cycling Network WFS
-	Source:  https://maps.stuttgart.de/stadtplan/ 
-	Web Feature Service: https://geoserver.stuttgart.de/geoserver/ows/
-	Extracted: September 13, 2026
-	542 Features, lines
-	Columns in German: Name, Route, Art, Fuehrungsf, Eingahnstr, Status, Karte, Stadtteil, Kommentar, Oberflaech, Richtung, SE_ANNO_CA (All Strings)
-	155 Nulls for Oberflaech (surface type), while the majority of the known data is made of Asphalt

  
## Air Pollution Data (NO2)
-	Source:  https://maps.stuttgart.de/stadtplan/ 
-	Web Feature Service: https://geoserver.stuttgart.de/geoserver/ows/
-	Extracted: September 13, 2026
-	114 Features, Polygon (Multipolygon)
-	Columns in German: GRIDCODE (real), ANNO_CAD_DATA (string), GRIDCODE_KLASSIFIZIEIRT (string)
-	No NULL values for concnetrations (GRIDCODE_KLASSIFIZIEIRT); data complete
