# gtfs2gpx

Convert route and stop data from GTFS csv-files to gpx tracks and waypoints.

## Usage

    gtfs2gpx <route_short_name>

This script must be run on a directory which contains unpacked GTFS data.
Produces files with names like `<route_short_name>_<shape_id>.gpx` for route
shape (gpx track) and `<route_short_name>_<shape_id>_stops.gpx` for stop
positions (gpx waypoints). See `routes.txt` in the GTFS data for a list of
routes.

## Requirements

 * gpsbabel (https://www.gpsbabel.org/ Debian: gpsbabel)
 * csvtool (https://github.com/Chris00/ocaml-csv Debian: csvtool)
 * Needs bash for PIPESTATUS

## Note

csvtool on Debian fails on files with unicode byte order mark (BOM).
Use bomstrip or similar to fix the GTFS .txt files in this case.
