osm-xml-schemas
===============

XML schemas for the [OSM XML](https://wiki.openstreetmap.org/wiki/OSM_XML) format.

The schemas can be used for validating large XML documents with the command line tool [xmllint](http://xmlsoft.org/xmllint.html) of the [libxml2](http://xmlsoft.org/) library.

## Using the schemas for validation

For example, let's grab the OSM XML extract for Budapest from [here](https://download.bbbike.org/osm/bbbike/Budapest/) and validate it with `xmllint`:

```bash
curl https://download.bbbike.org/osm/bbbike/Budapest/Budapest.osm.gz -O
gunzip Budapest.osm.gz
xmllint --stream --schema osm.xsd Budapest.osm
```

Note that the `--stream` command line option must be specified in order to read the input document in streaming mode.

## Further resources of interest

* [OpenStreetMap Wiki - Elements - Common attributes](https://wiki.openstreetmap.org/wiki/Elements#Common_attributes)
