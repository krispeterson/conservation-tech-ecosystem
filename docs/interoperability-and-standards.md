# Interoperability and Standards

This file focuses on the standards, schemas, and exchange formats that make conservation systems composable.

This matters because the field does not just need more tools. It needs tools that can exchange data without expensive custom glue.

## Biodiversity and ecological metadata standards

### Darwin Core (DwC)

One of the most important biodiversity information standards.

Use it for:

- occurrence data
- sampling-event data
- checklists
- many biodiversity publication workflows

Why it matters:

- it is the dominant shared vocabulary for biodiversity occurrence data
- it underpins a large share of GBIF publishing workflows
- OBIS also maps marine biodiversity data to Darwin Core

References:

- <https://dwc.tdwg.org/>
- <https://www.gbif.org/standards>

### Darwin Core Archive (DwC-A)

Packaging convention for sharing Darwin Core datasets.

Use it for:

- publishing biodiversity datasets to GBIF
- packaging occurrence and event data with extensions
- exchanging biodiversity datasets in a semi-standard way

References:

- <https://ipt.gbif.org/manual/en/ipt/latest/dwca-guide>
- <https://www.gbif.org/standards>

### EML (Ecological Metadata Language)

Metadata standard for ecological datasets.

Use it for:

- documenting datasets
- methods, coverage, contacts, and provenance
- metadata attached to biodiversity publications and archives

Why it matters:

- GBIF dataset descriptions rely on EML
- OBIS also uses EML for dataset metadata

References:

- <https://eml.ecoinformatics.org/>
- <https://www.gbif.org/standards>

### Audiovisual Core

TDWG vocabulary for biodiversity multimedia resources and collections.

Use it for:

- images
- audio
- video
- media metadata associated with biodiversity records

Why it matters:

- increasingly relevant as camera traps, acoustics, and image repositories grow
- useful companion to Darwin Core where media becomes first-class data

References:

- <https://www.tdwg.org/standards/ac/>
- <https://www.tdwg.org/community/ac/>

### ABCD / BioCASe

Older but still relevant collection-data standards and exchange infrastructure.

Use it for:

- natural history collections
- museum / institutional collection exchange
- legacy interoperability contexts

Reference:

- <https://www.gbif.org/standards>

### Humboldt Extension

Important newer work for biodiversity inventory data.

Why it matters:

- inventory and survey data often do not fit simple occurrence records cleanly
- this helps represent inventories more rigorously inside the Darwin Core ecosystem

Reference:

- <https://www.tdwg.org/community/osr/humboldt-extension/>

## Domain-specific exchange formats

### Camtrap DP

A major standard to watch for camera-trap data exchange.

A Camtrap DP is a Frictionless Data Package built around:

- `datapackage.json`
- `deployments.csv`
- `media.csv`
- `observations.csv`

Why it matters:

- camera-trap workflows badly need portable exchange formats
- Camtrap DP is one of the strongest current efforts to standardize that layer
- it is already connected to tooling and publication pathways

References:

- <https://camtrap-dp.tdwg.org/>
- <https://zenodo.org/records/13354921>

### Movebank data model

Not a formal standards body standard in the same sense as TDWG or OGC, but still important.

Why it matters:

- animal movement and biologging data are structurally complex
- Movebank has become a de facto data model and archive for a large amount of tracking work
- it is often more operationally relevant than a paper standard

Reference:

- <https://www.movebank.org/cms/movebank-content/mb-data-model>

### Passive acoustic monitoring (PAM) standards

This remains an area in motion rather than one settled standard.

What to watch:

- emerging common standards for PAM data discussed in WILDLABS and related communities
- use of Audiovisual Core and biodiversity publication pathways where possible
- practical packaging patterns around recordings, metadata, and detections

Reference starting points:

- <https://wildlabs.net/discussion/safe-and-sound-standard-bioacoustic-data>
- <https://www.tdwg.org/standards/ac/>

### Restoration outcome schemas

Still developing, but important for linking field data to reporting and finance.

What to watch:

- efforts to standardize metrics for restoration success (e.g., site-level vs. project-level outcomes)
- mappings to geospatial standards for interventions and monitoring
- integration with climate and biodiversity reporting frameworks

### Real-time alert and event formats

No dominant standard yet, but recurring needs in operational systems.

What to watch:

- OGC SensorThings API for sensor-based events
- custom schemas in platforms like EarthRanger and SMART
- efforts to standardize incident, patrol, and alert messages for cross-platform sharing

### Offline-first synchronization patterns

Not a formal standard, but a practical interoperability challenge.

What to watch:

- patterns for syncing data, media, and events in low-bandwidth environments
- prioritization and compression strategies
- conflict resolution for disconnected editing

Important adjacent area, especially for biodiversity monitoring.

What to watch:

- **MIxS** (Minimum Information about any (X) Sequence) from the Genomic Standards Consortium
- mappings or bridges between sequence metadata and biodiversity publication systems

Reference:

- <https://github.com/GenomicsStandardsConsortium/mixs>

## Geospatial interoperability standards

### OGC SensorThings API

Open, geospatially enabled API standard for IoT devices and observations.

Use it for:

- near-real-time sensor data
- heterogeneous sensor systems
- observation services that need modern web APIs

References:

- <https://www.ogc.org/standards/sensorthings/>
- <https://developers.sensorup.com/docs/>

### SensorML

Standard for describing sensors and processes associated with observations.

Use it for:

- sensor metadata
- processing chains
- measurement system description

Reference:

- <https://www.ogc.org/standards/sensorml/>

### Observations, Measurements, and Samples (O&M)

Conceptual model for describing observations and their results.

Use it for:

- structuring sensor observations
- aligning multi-sensor systems conceptually
- thinking more clearly about event, sample, and observation semantics

Reference:

- <https://www.ogc.org/standards/om/>

### STAC

SpatioTemporal Asset Catalog for geospatial asset metadata and discovery.

Use it for:

- imagery catalogs
- tiled and cloud-native geospatial assets
- discoverability across raster and derived products

References:

- <https://stacspec.org/>
- <https://www.ogc.org/standards/stac/>

### OGC API - Features

Standardized web API building blocks for feature data.

Use it for:

- sharing vector / feature data over the web
- interoperable geospatial APIs
- moving beyond older service patterns

Reference:

- <https://www.ogc.org/standards/ogcapi-features/>

### GeoPackage

Portable SQLite-based geospatial container.

Use it for:

- offline/mobile geospatial workflows
- compact field-ready transfer
- mixed vector, raster tiles, and attribute data

Reference:

- <https://www.geopackage.org/>

### GeoParquet

Columnar geospatial format based on Apache Parquet.

Use it for:

- large-scale analytics
- cloud and data-lake workflows
- interoperability with modern data engineering stacks

Reference:

- <https://geoparquet.org/>

### Cloud Optimized GeoTIFF (COG)

Cloud-friendly raster format and official OGC standard.

Use it for:

- remote sensing products
- cloud-native raster workflows
- efficient partial reads over HTTP/object storage

Reference:

- <https://www.earthdata.nasa.gov/about/esdis/esco/standards-practices/cloud-optimized-geotiff>

## Practical interoperability patterns

Not every useful interoperability layer is a formal standard.

In practice, common patterns include:

- CSV + controlled vocabularies
- REST/JSON APIs with geospatial conventions
- frictionless data packages
- DOI-backed publication workflows
- GitHub-hosted schemas and validators
- export bridges from operational platforms into GBIF / OBIS / GIS tools

## What is still missing

The ecosystem still lacks stronger shared conventions for:

- passive acoustic monitoring exchange
- cross-platform alert/event messages for near-real-time systems
- restoration outcome schemas
- easy mappings between field tools, camera trap systems, and biodiversity publication infrastructure
- consistent sensor metadata in low-resource deployments

## A simple rule of thumb

If you are building a new conservation system, try not to invent a new data model until you have checked:

1. TDWG standards
2. GBIF and OBIS publishing conventions
3. OGC APIs and geospatial standards
4. existing domain-specific efforts such as Camtrap DP and Movebank
5. whether your users already export to a format they trust

## See also

- [`docs/integration-patterns.md`](integration-patterns.md) — how these standards are used in practice
- [`docs/gaps-and-opportunities.md`](gaps-and-opportunities.md) — where standards are still missing
