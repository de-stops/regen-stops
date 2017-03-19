# regen-stops

This is a simple script to download [Regen](https://www.landkreis-regen.de/oepnv/158/3194/) stops as [GTFS-compatible CSV](https://developers.google.com/transit/gtfs/reference/stops-file).

The script uses the following endpoint:

```
http://www.bayern-fahrplan.de/XML_COORD_REQUEST?&jsonp=&boundingBox=&boundingBoxLU={minx}%3A{miny}%3AWGS84%5BDD.DDDDD%5D&boundingBoxRL={maxx}%3A{maxy}%3AWGS84%5BDD.DDDDD%5D&coordOutputFormat=WGS84%5BGGZHTXX%5D&type_1=STOP&outputFormat=json&inclFilter=1
```

It starts from bounding box `(12.7, 48.8, 13.5, 49.3)` and works down to smaller quadrants.

The script produces CSV output in the following format:

```
"stop_id","stop_name","stop_lon","stop_lat","stop_code"
"4110906","Zwiesel (Bay), Zwiesel, Lohmannmühle",13.2342480538,49.009043178899994,"de:9276:10906"
```

# Usage

```
npm install
npm run export
```

# Disclaimer

Usage of this script may or may not be legal, use on your own risk.  
This repository provides only source code, no data.

# License

Source code is licensed under [BSD 2-clause license](LICENSE). No license and no guarantees implied on the produced data, produce and use on your own risk.