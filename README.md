# Data journalism tools

In-progress list of tools and resources I find useful as a fledgling data journalist working in Bozeman, Montana. Half-intended as a way to organize personal notes/links, half-intended as a resource for others.

## Data cleaning/analysis

### Microsoft Excel

Near-ubiquitous data-wrangling tool. Can choke on large datasets, though.

Gotchas:
- With Mac version, save .csv files as "Windows Commas Separated (.csv)" instead of the default "Comma Separated Values (.csv)" to avoid strange encoding issues upon import into other programs like QGIS.

### csvkit

[Command-line tool](https://github.com/wireservice/csvkit) for working with .csv files. Handy when working with data that has strange encodings, with files that are too big for Excel to handle, or as a utility to prepare data for import into another program.

Resources:
- [Documentation](http://csvkit.readthedocs.org/)
- [Tutorial](http://csvkit.readthedocs.org/en/0.9.1/tutorial/1_getting_started.html), part of documentation.
- Also, a [good tutorial](http://learnpythonthehardway.org/book/appendixa.html) (From "Learn Python the Hard Way") for folks new to the command line

### Python

General-purpose programming language, with many libraries geared toward data cleaning/analysis tasks. (TODO: flesh this out)

Resources:
- [Codecademy](https://www.codecademy.com/) - web-based learn-to-code platform, teaching basics of web design and several programming languages
- Zed Shaw's ["Learn Python the Hard Way"](http://learnpythonthehardway.org/book/), a book-length tutorial detailing programming in Python
- [Refactoring101](http://refactoring-101.readthedocs.org/en/latest/) - Intermediate Python tutorial on converting linear scripts to easier-to-maintain modules

#### Anaconda Python distribution

A [version of the Python programming language](https://www.continuum.io/downloads) that comes with many commonly used data analysis libraries pre-installed. Geared primarily toward data scientists, but includes some tools that are also useful for data journalism.

Also includes iPython/Jupyter notebooks, a browser-based programming environment that's geared toward making trial and error easy.

TODO: Find a good tutorial to link to here

### Pandas

Python library that adds Series and DataFrame objects (giving the language data analysis abilities similar to R). Comes with the Anaconda distribution. Kind of a nasty learning curve, but powerful.

Resources:
- [10 minutes to Pandas](http://pandas.pydata.org/pandas-docs/stable/10min.html), introductory tutorial (assumes familiarity with Python)

#### Beautiful Soup

[Python library](http://www.crummy.com/software/BeautifulSoup/) for web scraping.

## Web-based visualization

### HTML/CSS/Javascript

Basic building blocks of the modern web. In a nutshell: HTML encodes information, CSS encodes styles and Javascript is a programming language used to provide interactivity.

Resources:
- [Codecademy](https://www.codecademy.com/) - web-based learn-to-code platform, teaching basics of web design and several programming languages (including HTML/CSS and Javascript)
- [Eloquent Javascript](http://eloquentjavascript.net/index.html) - free, book-length tutorial detailing Javascript functionality through an intermediate level.

### D3.js
Javascript library widely used for data manipulation and visualization, developed by a guy who spent some time working for the NY Times graphics department. Powerful, but with a steep learning curve.
 - Scott Murray's ["Interactive Data Visualization for the Web"](http://chimera.labs.oreilly.com/books/1230000000345/) - free web version of detailed introductory tutorial
 - [bl.ocks.org](http://bl.ocks.org/), repository for D3 examples put together by the library's author, Mike Bostock

## Mapping

### CartoDB

[Web-based service](https://cartodb.com/) for uploading/presenting geospatial data. User-friendly even without coding ability, and can produce iframe embeds that work OK even on mobile.

Resources:
- [CartoDB's in-house tutorial](http://academy.cartodb.com/)

### QGIS

[Free and open source desktop Geographic Information System (GIS)](http://qgis.org/en/site/), able to view/edit/render geographic data. Also suitable for exporting pdfs or static images for print/web publication.

Resources:
- [QGIS Tutorials and Tips](http://www.qgistutorials.com/en/) provides straightforward basic QGIS tutorials

Useful Extensions (can access through QGIS plugin manager):
- DB Manager - provides a graphic interface for working with external databases, like PostGIS
- OpenLayers - Lets you add Google streetmap or satellite imagery to your map as a layer
- CartoDB - Plugin for shuttling data between QGIS and CartoDB 

Gotchas:
- CRS (Coordinate Reference System) management can be tricky. (TODO: Add information about CRSs)
- Public agencies don't always have data available in formats that are easy to import into QGIS (it can generally handle ESRI shapefiles just fine, but I've had trouble with geo databases)
- Sometimes QGIS spatial analysis commands seem to fail or hang without explanation (and the program doesn't seem to be great about providing progress bars or kicking up error messages)

### PostGIS

[Spatial database system](http://postgis.net/) that interfaces with QGIS, technically an extension of [PostgreSQL](http://www.postgresql.org/), a flavor of SQL database. Allows you to manage/analyze geograpic data using SQL queries, and also seems to have more reliable spatial analysis capabilities than vanilla QGIS.

Resources:
- (Add tutorial I did)

### Mapshaper
Handy [web app](http://mapshaper.org/) for quick optimization of common geodata formats (Shapefile, GeoJSON, TopoJSON).

## Other tools

### Colorbrewer

[Web tool](http://colorbrewer2.org/) with pre-developed color palettes (including some that account for color-blindness). Geared toward cartography, but also works well for non-map graphics.

### Chartbuiler

[Web-based tool](https://quartz.github.io/Chartbuilder/) built by folks at Quartz that makes producing basic static charts super straighforward.

### Tableau

Reasonably easy-to-use [desktop app](http://www.tableau.com/) for exploring/visualizing data (Tableau Public is free; the full-scale professional version is available through IRE). Can also export interactive displays as iframes embeddeble on websites, but these tend not to be terribly mobile-friendly.