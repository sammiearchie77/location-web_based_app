# Make a Location-Based Web App With Django and GeoDjango

Throughout this tutorial, you’ll learn how to use Django and GeoDjango to build a location-based web application from scratch. You’ll be building a simple nearby shops application that lists the shops closest to a user’s location.

## The Tools You Will Be Using

You’ll be using the following tools to develop your nearby shops web application:

- The Python programming language
- The Django web framework
- The PostgreSQL database for persisting data
- The PostGIS extension for supporting spatial features in the PostgreSQL database
- pip for installing dependencies
- The venv module for managing a virtual environment
- Docker for installing PostgreSQL and PostGIS

Before diving into practical steps, let’s first start by introducing the frameworks you’ll be using.

[Django] is the most popular Python framework for building web apps. It makes it easy for developers to quickly build prototypes and meet their project deadlines by providing a plethora of built-in APIs and sub-frameworks such as GeoDjango.

[GeoDjango] is a built-in application that is included as a contrib module in Django. It’s actually a complete framework itself that can also be used separately from Django. It provides a toolbox of utilities for building GIS web applications.

[GIS] stands for Geographic Information System. It’s an information system (an organized system for the collection, organization, storage, and communication of information) designed for processing and manipulating data that have geographic or spatial characteristics.

[GeoDjango] also provides Python bindings to popular spatial libraries such as GEOS, GDAL, and GeoIP, which can be used separately without Django in any Python application or interactively in the shell.

GeoDjango aims to provide a world-class geographic web framework. It has been refactored over the years with the goal of making it easier to work with geospatial data, in other words data that identifies the geographic location of natural or artificial features on Earth and is stored as coordinates and topologies.

GeoDjango integrates very well with the Django ORM and provides a set of geometry fields defined by the Open Geospatial Consortium (OGS) that can be used to map to different types of geometries in geospatial databases:

- GeometryField is the base class for all geometric fields in GeoDjango.
- PointField is used for storing GEOS Point objects.
- PolygonField is used for storing GEOS Polygon objects and so on.

[GeoDjango] is a very powerful framework for storing and working with geographic data using the Django ORM. It  provides an easy-to-use API to find the distances between two points on a map, areas of polygons, the points within a polygon, and so on.

To be able to work with GeoDjango, you’ll need to have two things: a spatial database and geospatial libraries. A spatial database is a database that is optimized for storing and querying data that represents objects defined in a geometric space.

To fully use all features of GeoDjango, you’ll need to install the following open-source geospatial libraries:

- GEOS stands for Geometry Engine Open Source. It’s a C++ port of the JTS (Java Topology Suite) that implements the OCG Simple Feature for SQL specification.

- GDAL stands for Geospatial Data Abstraction Library. It’s an open-source library for working with raster and vector geospatial data formats.

- PROJ.4 is for Cartographic Projections library. It’s an open-source GIS library for easily working with spatial reference systems and projections.

- GeoIP is a library that helps users find geographical information based on an IP address.

This tutorial makes use of an Ubuntu 18.04 system for installing prerequisites and a Unix bash for running the commands, but this shouldn’t be a problem for you if you’re using any other system, particularly Unix-based systems like macOS.

## Prerequisites

In this section, you’ll be installing the prerequisites needed before you can bootstrap your project, such as Python 3 and GeoDjango dependencies (GEOS, GDAL, and PROJ.4). You’ll also use Docker to set up a PostgreSQL and PostGIS database for your project.