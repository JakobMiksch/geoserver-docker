# GeoServer Docker

A [GeoServer](http://geoserver.org/) Docker Image with predefined extensions.

GeoServer is an open source server for sharing geospatial data. Designed for interoperability, it publishes data from any major spatial data source using open standards.

## Run as container

By running

```shell
docker run -p 18080:8080 meggsimum/geoserver:2.15.2
```

you'll get a cleaned standard GeoServer, which can be accessed by http://localhost:18080/geoserver

## Shipped Extensions

This Docker Image comes with several extensions which are bundled in:

  - WPS
  - Vector Tiles
  - Imagemosaic JDBC

These extensions can be activated by the following environment variables:

  - `USE_WPS=1`
  - `USE_VECTOR_TILES=1`
  - `USE_IMG_MOSAIC=1`

By running

```shell
docker run -e USE_WPS=1 -e USE_VECTOR_TILES=1 -p 18080:8080 meggsimum/geoserver:2.15.2
```

you'll get a GeoServer with installed and activated WPS and Vector Tiles extension.

## Credits
This GeoServer Docker Image was heavily inspired by the one here: https://github.com/terrestris/docker-geoserver/ of the [terrestris](https://github.com/terrestris) organization. Thank you!
