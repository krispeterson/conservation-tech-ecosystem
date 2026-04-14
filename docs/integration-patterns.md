# Integration Patterns

This file focuses on how conservation systems connect in practice.

A taxonomy of tools is helpful, but it is not enough. People need to know how data and events actually move across devices, field apps, operational platforms, archives, analytical systems, and public biodiversity infrastructure.

These patterns are not rigid reference architectures. They are recurring shapes that show up across the sector.

## Why this matters

Conservation systems often fail at the seams.

The hard part is usually not collecting a photo, a detection, a patrol record, or a GPS point. The hard part is getting that information into the next system without brittle one-off scripts, metadata loss, or manual cleanup.

A useful conservation-tech stack should usually answer five questions:

1. how is data collected or generated?
2. where is it validated or enriched?
3. where is it used operationally?
4. where is it archived or published?
5. what standard or exchange format connects those steps?

## Pattern 1: Citizen science observation to biodiversity publication

**Typical flow**

1. Observation captured in a community-facing tool such as iNaturalist, eBird, or CitSci.org
2. Community review, expert validation, or platform QA
3. Export or synchronization into biodiversity data infrastructure
4. Publication or aggregation through GBIF or domain-specific downstream systems

**Common building blocks**

- observation platforms
- taxonomic reference backbones
- Darwin Core terms
- EML dataset metadata
- GBIF publishing workflows

**Where it breaks**

- taxonomic mismatches
- missing effort metadata
- uncertain provenance after manual export
- weak alignment between project-specific fields and standard biodiversity vocabularies

**Design advice**

If you are building a citizen-science or field-observation app, assume that users will eventually want a Darwin Core-aligned export, even if they do not ask for it on day one.

## Pattern 2: Camera trap workflow to archive and analysis

**Typical flow**

1. Images collected from camera traps in the field
2. Media ingested into a management or annotation platform
3. Model inference or human review produces detections or observations
4. Data packaged for reuse, analysis, or publication
5. Selected outputs move into biodiversity infrastructure or downstream analytics

**Common building blocks**

- Wildlife Insights
- Wildbook and related visual-ID systems
- Agouti / TRAPPER-style camera trap workflows
- Camtrap DP
- Audiovisual Core
- Darwin Core mappings for derived observations

**Where it breaks**

- different folder conventions and metadata structures
- model outputs that are hard to trace back to source images
- poor portability between camera-trap platforms
- weak mappings from image events to biodiversity publication systems

**Design advice**

Support Camtrap DP export early. Even partial support is better than inventing a private packaging scheme that nobody else understands.

## Pattern 3: Passive acoustic monitoring to detection pipeline

**Typical flow**

1. Field devices collect raw audio
2. Audio and deployment metadata are synchronized to local or cloud storage
3. Detection, classification, or review happens in BirdNET, Arbimon, or custom workflows
4. Derived detections are summarized for analysis, reporting, or publication
5. Selected outputs are linked to biodiversity records, media repositories, or operational dashboards

**Common building blocks**

- AudioMoth and other PAM recorders
- BirdNET
- Arbimon
- Audiovisual Core
- storage conventions for recordings plus deployment metadata

**Where it breaks**

- raw recordings and derived detections are often separated poorly
- metadata about deployment, habitat, effort, and calibration is inconsistent
- there is no universally dominant exchange package comparable to Camtrap DP
- publication pathways are weaker than they should be

**Design advice**

Keep raw recordings, deployment metadata, model version, and derived detections linked by stable identifiers. Without that, reproducibility and reuse collapse quickly.

## Pattern 4: Animal tracking and biologging to movement archive

**Typical flow**

1. Tags or collars generate GPS, Argos, acoustic telemetry, or sensor time series
2. Data is transmitted or manually offloaded
3. Cleaning, gap handling, and device metadata reconciliation are performed
4. Data is analyzed in movement workflows and optionally deposited in a long-term archive
5. Results feed research, marine or terrestrial operations, and downstream modeling

**Common building blocks**

- Movebank
- device vendor exports
- time-series QA workflows
- geospatial analytics environments

**Where it breaks**

- vendor-specific formats
- inconsistent sensor metadata
- unclear relationships among locations, behavioral events, and environmental covariates
- difficulty combining biologging and broader operational platforms

**Design advice**

Treat the device export as a source artifact, not the canonical model. Normalize early, preserve provenance, and keep sensor metadata intact.

## Pattern 5: Protected-area operations and near-real-time alerts

**Typical flow**

1. Patrol, incident, or sensor data is captured in field tools or edge devices
2. Records flow into operational platforms such as SMART or EarthRanger
3. Alerts, incidents, or tasking workflows are generated
4. Data is reviewed in dashboards and operational coordination views
5. Selected summaries or evidence are exported to reporting, planning, or external systems

**Common building blocks**

- SMART
- SMART Connect
- EarthRanger
- telemetry feeds
- geofencing and alert rules
- GIS layers and web maps

**Where it breaks**

- no common cross-platform event message format
- duplicate concepts for incidents, patrols, alerts, and observations
- integration often relies on custom ETL or API adapters
- operational urgency pushes teams toward shortcuts that later become technical debt

**Design advice**

Separate the operational event model from the UI. Teams often hard-wire alert semantics into a single dashboard, which makes future integration much harder.

## Pattern 6: Edge AI alerting in low-connectivity environments

**Typical flow**

1. Low-power edge device collects image, audio, or other sensor signal
2. On-device or near-device inference produces a detection
3. Detection is filtered, compressed, and prioritized
4. Alert or summary travels over intermittent cellular, radio, satellite, or store-and-forward links
5. Central system receives the event and routes it into operational workflows

**Common building blocks**

- TrailGuard AI-style systems
- embedded vision or acoustic models
- small-form-factor Linux or MCU hardware
- event queues, message brokers, or lightweight HTTP/JSON endpoints
- EarthRanger or similar downstream operations platforms

**Where it breaks**

- bandwidth and power constraints
- model drift in the field
- weak remote observability and device management
- ad hoc event schemas with little reuse
- limited support for offline-first synchronization

**Design advice**

Design the event payload first. In low-connectivity deployments, the event is the product. The raw media may never arrive in time to matter operationally.

## Pattern 7: Restoration monitoring and reporting

**Typical flow**

1. Field plots, participatory mapping, and remote sensing data are collected
2. Land units, interventions, and baseline conditions are harmonized
3. Monitoring results are analyzed in restoration or forest-monitoring ecosystems
4. Outputs are used for planning, grant reporting, carbon or biodiversity claims, and adaptive management
5. Data is shared with partners, funders, or public-facing reporting systems

**Common building blocks**

- Open Foris tools
- SEPAL
- Collect Earth Online
- TerrAdapt
- geospatial layers, raster products, and field observations

**Where it breaks**

- weakly standardized outcome schemas
- inconsistent definitions of restoration success
- hard joins between field data, polygons, interventions, and time-series imagery
- disconnected climate, biodiversity, and social-impact reporting models

**Design advice**

Be explicit about the unit of reporting. Many restoration systems quietly mix site, parcel, plot, intervention, and project-level metrics in ways that make later comparison very messy.

## Pattern 8: Marine monitoring and fisheries transparency

**Typical flow**

1. Vessel tracks, remote sensing, observer data, or species observations are collected
2. Human activity and biodiversity data are processed in separate pipelines
3. Marine platforms aggregate events, detections, or biodiversity occurrences
4. Outputs inform enforcement, protected-area planning, transparency, or science products
5. Select datasets flow into marine infrastructure such as OBIS or public transparency systems

**Common building blocks**

- Global Fishing Watch
- OBIS
- remote sensing and AIS-derived products
- marine species observation systems
- image or acoustic analysis for marine mammals and reefs

**Where it breaks**

- operational and biodiversity pipelines often stay disconnected
- marine spatial data is technically interoperable but organizationally siloed
- metadata quality varies sharply across jurisdictions and programs

**Design advice**

Do not assume that vessel monitoring data and biodiversity records will be managed by the same people. The integration challenge is as much institutional as technical.

## Pattern 9: Geospatial asset pipeline for analysis and delivery

**Typical flow**

1. Raster, vector, and sensor products are generated from remote sensing or field workflows
2. Assets are stored in cloud or offline packages
3. Catalog metadata is published for discovery
4. Data is served into desktop GIS, web maps, dashboards, and analytics systems
5. Downstream teams derive reports, alerts, or models from the same assets

**Common building blocks**

- STAC
- COG
- GeoPackage
- GeoParquet
- OGC API - Features
- QGIS

**Where it breaks**

- asset discovery is inconsistent
- field teams need offline formats while analysts prefer cloud-native ones
- many systems still publish derived products with little lineage metadata

**Design advice**

Use cloud-native formats where possible, but always provide an escape hatch for offline users. In conservation, disconnected workflows are not an edge case.

## A lightweight reference architecture

A pragmatic pattern that fits a large share of conservation systems:

- **collection layer** — field apps, devices, sensors, community platforms
- **validation and enrichment layer** — QA, labeling, taxonomic review, inference, metadata cleaning
- **operational layer** — alerts, patrol systems, dashboards, decision support
- **archive and publication layer** — GBIF, OBIS, Movebank, institutional repositories
- **interoperability layer** — Darwin Core, EML, Camtrap DP, OGC APIs, STAC, GeoPackage, GeoParquet

This is intentionally boring. Boring is good. Conservation stacks benefit from simple seams more than clever abstractions.

## Where the field still needs stronger shared patterns

The biggest gaps remain:

- common event/message formats for real-time conservation operations
- better portable packaging for passive acoustic monitoring
- stronger mappings from camera trap and acoustic outputs into biodiversity publication systems
- restoration data models that carry interventions, outcomes, uncertainty, and provenance cleanly
- repeatable offline-first synchronization patterns for low-bandwidth field deployments

## What to do when designing a new system

Before inventing a new model or API, ask:

1. Can the core observation or event map to an existing biodiversity or geospatial standard?
2. What is the stable identifier for the source artifact, deployment, site, or device?
3. Can the data be exported in a package another team can understand without your UI?
4. Will the workflow still function when connectivity is intermittent for days or weeks?
5. Can the outputs be published or archived without hand-editing spreadsheets?

## See also

- [`docs/interoperability-and-standards.md`](interoperability-and-standards.md) — standards that enable these patterns
- [`docs/gaps-and-opportunities.md`](gaps-and-opportunities.md) — where patterns are still weak
