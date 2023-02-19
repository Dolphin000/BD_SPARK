# BD_SPARK
Created Spark etl job to read data from a storage container
For incorrect values, mapped Latitude & Longitude from OpenCage Geocoding API in job on the fly (Via REST API).
Generated geohash by Latitude & Longitude using one of geohash libraries (like geohash-java) with the four-character length in an extra column.
Left joined weather and hotels data by generated 4-characters geohash, by dropping duplicates of Geohash and lat and lng columns from the weather data
