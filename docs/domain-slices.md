# Domain Slices

This file tightens the taxonomy by grouping the ecosystem into problem spaces that practitioners actually work in.

A single product may appear in multiple sections. That is normal. Conservation technology is not cleanly segmented.

## Protected area operations and ranger workflows

These platforms are closest to day-to-day operational conservation.

- **SMART** — patrol planning, law-enforcement monitoring, ecological surveys, protected area reporting
- **SMART Connect** — connected workflows and data sharing layer for SMART deployments
- **EarthRanger** — real-time monitoring, alerts, personnel safety, wildlife tracking, human-wildlife conflict workflows
- **SERCA** — alliance layer connecting SMART and EarthRanger ecosystems

Why this slice matters:

- It is where conservation technology becomes operational rather than purely analytical.
- It is also where interoperability failures become painfully obvious.

## Biodiversity observation and citizen science

These platforms create large-scale biodiversity data and public participation.

- **iNaturalist**
- **eBird**
- **CitSci.org**
- **GBIF**
- **WILDLABS** (community/discovery rather than observation platform, but still central)

Common patterns:

- species observations
- photo/audio uploads
- community validation and expert review
- export to broader biodiversity infrastructure

## Camera traps, wildlife imagery, and visual annotation

This slice includes both operational platforms and the data-exchange standards around them.

### Platforms and systems

- **Wildlife Insights**
- **Wildbook**
- **Wild Me**
- **Flukebook**
- **CoralNet** — benthic image annotation and repository platform for coral reef analysis
- **Agouti** and **TRAPPER** — important to watch because of their relevance to camera trap workflows and standards adoption

### Why this slice is important

- Camera trap workflows have become one of the most active areas of conservation automation.
- The next bottleneck is not image collection. It is exchange, QA, validation, and downstream interoperability.

## Bioacoustics and passive acoustic monitoring

One of the fastest-moving areas in conservation technology.

### Platforms, tools, and hardware

- **Open Acoustic Devices / AudioMoth**
- **BirdNET**
- **Arbimon** — proprietary / hosted acoustic analysis platform
- **whoot** and related bioacoustic repos in the Conservation Technology Lab ecosystem
- **FinDrop** and other niche aquatic-acoustics efforts worth watching

### Current state

This domain is strong in sensors, models, and workflows, but still weaker than it should be in widely adopted data standards and exchange formats.

## Marine conservation and ocean monitoring

Marine conservation has its own stack and should not be treated as a side note.

### Important platforms and infrastructures

- **OBIS** — marine biodiversity data infrastructure
- **Global Fishing Watch** — open-access monitoring and analysis of human activity at sea
- **Flukebook** — cetacean photo-ID and collaboration
- **CoralNet** — coral reef benthic image analysis
- **Movebank** — relevant where animal movement and tagging cross into marine systems
- **Tech4Nature** marine pilots and related partnerships

### Common subproblems

- marine protected area planning and enforcement
- vessel activity monitoring
- marine mammal identification and acoustic detection
- reef imagery analysis
- biologging and telemetry

## Fisheries and seafood transparency

This is adjacent to conservation technology but deserves its own category because the actors, data, and incentives differ.

### Core systems to watch

- **Global Fishing Watch**
- vessel tracking / AIS analysis systems
- marine protected area compliance tools
- port-state monitoring and fisheries enforcement analytics

### Notes

This area overlaps heavily with remote sensing, satellite analytics, public transparency, and government compliance workflows.

## Restoration, forests, and land-use monitoring

This domain is larger than “tree planting” and increasingly important.

### Major ecosystems

- **Open Foris**
  - **Collect**
  - **Collect Earth**
  - **Collect Earth Online**
  - **Arena**
  - **Ground**
  - **SEPAL**
  - **FERM**
- **TerrAdapt**
- **Restor** — restoration-focused planning / monitoring ecosystem to watch

### Why this slice matters

Restoration work increasingly requires:

- large-scale remote sensing
- collaborative interpretation workflows
- field verification
- transparent reporting
- links to climate, biodiversity, and finance outcomes

## Animal movement, telemetry, and biologging

This is a foundational but often under-listed category.

- **Movebank**
- on-animal sensor data infrastructures
- acoustic telemetry, GPS, Argos, geolocators, and related movement-analysis workflows

This domain is especially important because it forces attention to sensor metadata, event modeling, time series, and long-term archiving.

## Ecological interactions, food webs, and biodiversity knowledge graphs

This slice covers systems that represent relationships among organisms, such as predation, pollination, parasitism, host relationships, herbivory, mutualism, and broader literature-derived biodiversity claims.

### Important databases and graph layers

- **Global Biotic Interactions (GloBI)** — broad open index of species interaction records with source provenance
- **Mangal** — ecological interaction database and API oriented toward ecological network analysis
- **Web of Life** — downloadable ecological network matrices across food webs, pollination, seed dispersal, host-parasite, plant-herbivore, and related networks
- **OpenBiodiv** — literature-derived biodiversity knowledge graph using semantic publishing and linked open data
- **EltonTraits** — trait layer for bird and mammal foraging ecology that can support ecological-role inference, though it is not a pairwise interaction graph

### Why this slice matters

Ecological relationship data can help conservation systems move beyond “where is this species?” toward “what depends on this species, habitat, or intervention?” For decision-support systems, these databases are best treated as evidence-backed relationship layers rather than complete ecosystem truth.

### Common caveats

- interactions are context-dependent by geography, season, habitat, life stage, disturbance, and scarcity
- coverage is uneven across taxa and regions
- source provenance, confidence, and citation metadata matter as much as the interaction label

## Edge AI and embedded conservation systems

This is a technical slice rather than a biological one.

### Representative systems

- **TrailGuard AI** — on-device detection and alerting
- **tinyscrubcam** — edge-AI wildlife detection workflow from Conservation Technology Lab
- **BirdNET embedded models**
- **AudioMoth** derivative firmware and field customizations
- custom low-power systems built around Raspberry Pi, MCUs, and cellular/satellite links

### Why this matters

The edge is where conservation constraints become real:

- low power
- intermittent connectivity
- ruggedization
- local inference
- privacy / security / anti-poaching concerns
- sparse technical support in the field

## Geospatial interoperability and analysis infrastructure

This is cross-cutting, but it deserves explicit treatment.

### Common building blocks

- **QGIS**
- **STAC**
- **OGC API - Features**
- **GeoPackage**
- **GeoParquet**
- **Cloud Optimized GeoTIFF**
- **SensorThings API**

### Why it matters

Conservation tech often fails not because models are weak, but because data cannot move cleanly among:

- field apps
- databases
- imagery pipelines
- GIS tools
- dashboards
- reporting systems

## Where the ecosystem still feels thin

The most obvious weak spots right now:

- bioacoustic data standards
- camera-trap interoperability outside the leading standards discussions
- shared schemas for restoration outcomes
- cleaner links between field apps and biodiversity publication pipelines

## See also

- [`docs/interoperability-and-standards.md`](interoperability-and-standards.md) — standards for these domains
- [`docs/gaps-and-opportunities.md`](gaps-and-opportunities.md) — opportunities in weak areas
- consistent event/message formats for near-real-time alerting
