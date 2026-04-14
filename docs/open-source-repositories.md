# Open-Source Repositories

This section goes one step deeper than the platform landscape.

The point is not to dump every repo vaguely related to wildlife or ecology. The point is to highlight repositories and GitHub organizations that are either:

- directly tied to important conservation platforms
- useful as integration points, APIs, or analysis libraries
- maintained by credible organizations or labs
- small but active enough to deserve attention

Projects with no visible usage, no maintenance signal, and no clear ecosystem role are usually not included.

## Selection philosophy

This file uses a practical filter rather than a rigid numeric threshold.

Positive signals include:

- a real conservation workflow behind the code
- recognizable organizational provenance
- signs of community reuse or discoverability
- recent activity
- usable documentation
- integration relevance to a broader ecosystem

That still leaves room to include some smaller projects that are early but promising.

## Foundational repositories and organizations

### Wild Me / Wildbook ecosystem

- **WildMeOrg/Wildbook**  
  Main open-source Wildbook framework for wildlife data management and identification workflows.  
  <https://github.com/WildMeOrg/Wildbook>

- **WildMeOrg/wildbook-ia**  
  Machine-learning and image-analysis backend for the Wildbook ecosystem.  
  <https://github.com/WildMeOrg/wildbook-ia>

Why it matters:

- This is one of the clearest examples of a conservation platform with real open-source depth.
- The stack bridges biodiversity workflows, image analysis, animal re-identification, and research collaboration.

### Open Acoustic Devices / AudioMoth ecosystem

- **OpenAcousticDevices**  
  Organization with firmware, utilities, configuration apps, and supporting tooling around AudioMoth devices.  
  <https://github.com/OpenAcousticDevices>

- **OpenAcousticDevices/AudioMoth-Project**  
  Base project used to build AudioMoth firmware.  
  <https://github.com/OpenAcousticDevices/AudioMoth-Project>

- **OpenAcousticDevices/AudioMoth-Firmware-Basic**  
  Basic firmware for AudioMoth devices.  
  <https://github.com/OpenAcousticDevices/AudioMoth-Firmware-Basic>

Why it matters:

- AudioMoth is one of the best-known open hardware ecosystems in biodiversity acoustics.
- These repos are useful not only for deployment, but also for derivative tooling and field adaptation.

### Mothbox ecosystem

- **Digital-Naturalism-Laboratories/Mothbox**  
  Hardware, documentation, AI-assisted insect monitoring workflow, and build materials.  
  <https://github.com/Digital-Naturalism-Laboratories/Mothbox>

Why it matters:

- Strong example of a modern open conservation hardware project that combines physical build docs with downstream machine-learning workflow support.
- Especially worth watching because it appears to be actively restructuring and growing.

### iNaturalist ecosystem

- **inaturalist/inaturalist**  
  The open-source Rails app behind iNaturalist.org.  
  <https://github.com/inaturalist/inaturalist>

- **inaturalist/iNaturalistAPI**  
  Node.js API service for iNaturalist.  
  <https://github.com/inaturalist/iNaturalistAPI>

- **inaturalist/inaturalist-open-data**  
  Documentation for iNaturalist open datasets.  
  <https://github.com/inaturalist/inaturalist-open-data>

- **pyinat/pyinaturalist**  
  Well-known Python client for the iNaturalist API.  
  <https://github.com/pyinat/pyinaturalist>

Why it matters:

- iNaturalist is one of the most consequential biodiversity data-generation platforms in the world.
- The surrounding repositories matter for integrations, analytics, app development, and downstream research tooling.

### eBird / Cornell ecosystem

- **ebird/ebirdst**  
  R package and documentation ecosystem for working with eBird Status and Trends data.  
  <https://github.com/ebird/ebirdst>

- **CornellLabofOrnithology/auk**  
  R package for working with large eBird datasets.  
  <https://github.com/CornellLabofOrnithology/auk>

- **birdnet-team/BirdNET-Analyzer**  
  Open BirdNET analyzer for scientific audio processing and bioacoustic workflows.  
  <https://github.com/birdnet-team/BirdNET-Analyzer>

Why it matters:

- These are some of the most practical open research/data-analysis tools attached to major biodiversity observation and bioacoustics platforms.
- They are especially useful for analysts, modelers, and applied science teams.

### Open Foris ecosystem

- **openforis**  
  Broad organization behind a major open ecosystem for forest and land monitoring.  
  <https://github.com/openforis>

Highlighted repos:

- **collect-earth** — desktop visual interpretation
- **collect-earth-online** — collaborative web interpretation
- **collect** — survey design and field data management
- **arena** — cloud-based field inventory / questionnaire platform
- **ground-platform** — field and ground data workflows
- **sepal** — cloud geodata processing environment

Why it matters:

- This is one of the strongest open-source ecosystems in restoration, forestry, and land-use monitoring.
- It combines field data collection, remote sensing, collaborative interpretation, QA/QC, and downstream reporting.

### Conservation Technology Lab

- **conservationtechlab**  
  GitHub organization from the San Diego Zoo Wildlife Alliance’s Conservation Technology Lab.  
  <https://github.com/conservationtechlab>

Highlighted repos:

- **animl-r** — machine-learning tools for ecological data  
- **animl-py** — Python package for ecological image classification workflows  
- **whoot** — tools for bioacoustic data capture and parsing  
- **cougarvision** — automated image/video analysis for field cameras  
- **tinyscrubcam** — edge-AI device and workflow for wildlife detection and alerts

Why it matters:

- This is exactly the kind of organization-level GitHub presence that is easy to miss but highly valuable.
- The projects are small-to-mid scale, but they are clearly connected to real conservation use cases.

## Standards and interoperability repositories worth tracking

These are not always flashy applications, but they matter because they help the ecosystem connect.

- **tdwg/camtrap-dp** — camera trap data exchange standard  
  <https://github.com/tdwg/camtrap-dp>

- **stac-utils**, **stac-spec**, and related STAC ecosystem repos — geospatial asset cataloging and interoperability  
  <https://github.com/radiantearth/stac-spec>

- **GeoParquet** spec repo  
  <https://github.com/opengeospatial/geoparquet>

Why these matter:

- They reduce lock-in.
- They give tool builders something to align to.
- They are often more strategically important than yet another isolated dashboard.

## Promising smaller or niche repos

These are not necessarily foundational platforms, but they can be useful and deserve visibility.

- **ConservationInternational/cplus-plugin**  
  QGIS plugin from Conservation International.  
  <https://github.com/ConservationInternational/cplus-plugin>

- **RJGrayEcology/smartR**  
  Reproducible analysis snippets for SMART workflows.  
  <https://github.com/RJGrayEcology/smartR>

- **pyinat/naturtag**  
  Tooling to tag nature photos with iNaturalist-linked taxonomy metadata.  
  <https://github.com/pyinat/naturtag>

- **wildlife-dynamics**  
  Workflow-oriented repositories built around EarthRanger-derived wildlife and patrol analysis.  
  <https://github.com/wildlife-dynamics>

- **CoralNet source / related repos**  
  Worth watching for marine image analysis and reef annotation workflows.  
  <https://github.com/coralnet>

- **iobis/robis**  
  R package for accessing OBIS data programmatically.  
  <https://github.com/iobis/robis>

### Why these make the cut

They are not huge projects, but they have at least one of the following:

- real organizational provenance
- a clear operational conservation use case
- recent activity
- practical reuse potential for others

That is enough to justify exposure.

## What is intentionally excluded

This section generally avoids:

- class projects and abandoned demos
- generic ML repos with no conservation-specific value
- one-off scripts with no documentation or reuse path
- repos that are technically public but operationally dead

## Good future expansions

- more marine conservation and fisheries tooling
- more restoration and landscape monitoring repositories
- separate treatment for telemetry / biologging code ecosystems
- better coverage of mobile-first field data collection stacks
- a dedicated section on schemas, validators, and data-conversion utilities

## See also

- [`docs/interoperability-and-standards.md`](interoperability-and-standards.md) — standards these repos often implement
- [`docs/integration-patterns.md`](integration-patterns.md) — how these repos fit into workflows
