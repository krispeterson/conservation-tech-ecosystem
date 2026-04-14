# Landscape

## Learning, discovery, and field orientation

### WILDLABS

- **WILDLABS**  
  Global conservation technology community with discussions, groups, events, and learning resources.  
  <https://wildlabs.net/>

- **Introduction to Conservation Technology**  
  A useful starting course covering hardware, software, data, ethics, and sector challenges.  
  <https://wildlabs.net/courses/introduction-conservation-technology>

- **The Inventory**  
  Wiki-style discovery platform for conservation technology products, organizations, and R&D efforts.  
  <https://wildlabs.net/inventory>

---

## Major conservation technology platforms

### Protected area operations and management

- **SMART (Spatial Monitoring and Reporting Tool)** — open source / non-proprietary  
  Widely used for patrol management, law-enforcement monitoring, protected area workflows, ecological surveys, and conservation reporting.  
  <https://smartconservationtools.org/en-us/>

- **SMART Connect** — managed extension / connected operations layer  
  Adds real-time data transfer, reporting, and sharing capabilities to SMART workflows.  
  <https://smartconservationtools.org/en-us/Download/SMART-Connect>

- **EarthRanger** — operational software platform  
  Real-time software for wildlife monitoring, protected area management, human-wildlife conflict response, personnel safety, and habitat protection.  
  <https://www.earthranger.com/>

- **TerrAdapt** — cloud planning and spatial decision-support  
  Spatial decision-support for monitoring, forecasting, and prioritization under landscape and climate change.  
  <https://terradapt.org/>

### Camera trap, image analysis, and wildlife identification

- **Wildlife Insights** — camera-trap platform with AI  
  Upload, manage, analyze, map, store, and share camera trap data with machine learning assistance.  
  <https://www.wildlifeinsights.org/home>

- **Wildbook** — open-source wildlife data framework  
  Supports mark-recapture, social ecology, molecular ecology, and individual animal identification workflows.  
  <https://wildbook.org/>

- **Wild Me** — open software + AI ecosystem  
  Builds software and machine-learning tools for wildlife research, identification, and population assessment.  
  <https://www.wildme.org/>

- **Flukebook**  
  Cetacean photo-identification and collaboration platform built within the Wild Me ecosystem.  
  <https://www.flukebook.org/>

- **CoralNet**  
  Free, open-source benthic image analysis and collaboration platform for coral reef annotation workflows.  
  <https://coralnet.ucsd.edu/>

### Citizen science and biodiversity observation

- **iNaturalist**  
  One of the most important global biodiversity observation platforms, with direct value for education, engagement, biodiversity data generation, and downstream analysis.  
  <https://www.inaturalist.org/>

- **eBird**  
  Core bird observation and analysis ecosystem with open data products and strong research utility.  
  <https://science.ebird.org/en/use-ebird-data>

- **CitSci.org**  
  A citizen science support platform for creating, managing, analyzing, and reporting community science projects, including mobile/offline workflows.  
  <https://www.citsci.org/>

### Open biodiversity and movement-data infrastructure

- **GBIF (Global Biodiversity Information Facility)**  
  International data infrastructure providing open access to biodiversity occurrence and dataset information.  
  <https://www.gbif.org/>

- **OBIS (Ocean Biodiversity Information System)**  
  Open-access marine biodiversity data infrastructure.  
  <https://obis.org/>

- **Movebank**  
  Major platform for managing, sharing, analyzing, and archiving animal tracking and animal-borne sensor data.  
  <https://www.movebank.org/>

### Forests, restoration, and land monitoring

- **Open Foris**  
  Large open-source ecosystem for forest and land monitoring.  
  <https://openforis.org/>

- **Collect Earth**  
  Desktop-oriented visual interpretation workflow for land monitoring and change assessment.  
  <https://openforis.org/solutions/collect-earth/>

- **Collect Earth Online**  
  Web-based geospatial interpretation platform for collaborative monitoring, QA/QC, and reference-data generation.  
  <https://www.openforis.org/collect-earth-online/>

- **FERM**  
  Restoration-focused registry and geospatial tool for documenting and monitoring restoration activities across ecosystems.  
  <https://openforis.org/solutions/ferm/>

- **Restor**  
  Restoration-oriented platform worth tracking for ecosystem restoration and biodiversity monitoring workflows.  
  <https://restor.eco/>

### Marine and fisheries monitoring

- **Global Fishing Watch**  
  Open-access map, data, and analysis platform for human activity at sea, fisheries transparency, and marine protection workflows.  
  <https://globalfishingwatch.org/>

---

## Open-source hardware and field devices

- **Open Acoustic Devices / AudioMoth**  
  Low-cost open-source acoustic monitoring ecosystem used widely in biodiversity and environmental monitoring.  
  <https://www.openacousticdevices.info/>

- **Mothbox**  
  Low-cost open-source insect monitoring system with hardware, field documentation, and AI-assisted processing.  
  <https://digital-naturalism-laboratories.github.io/Mothbox/>

- **GOSH (Gathering for Open Science Hardware)**  
  Key community infrastructure for open scientific hardware, repairability, documentation, and collaborative device development.  
  <https://openhardware.science/>

---

## Useful open data and analysis layers

These are not always “conservation tech platforms” in the operational sense, but they are core parts of the stack.

- **GBIF APIs and datasets** — biodiversity occurrence and dataset access
- **OBIS APIs and datasets** — marine biodiversity access
- **Movebank data archive** — tracking and biologging data
- **eBird data products** — bird distribution, abundance, and trend products
- **iNaturalist API and open datasets** — species observations and image-linked biodiversity data
- **QGIS ecosystem** — crucial for practical geospatial workflows in conservation projects

---

## Cross-cutting standards and interoperability layers

If you are evaluating a platform, do not just ask whether it has features. Ask whether it can exchange data.

Key things to know:

- **Darwin Core / Darwin Core Archive** — biodiversity exchange
- **EML** — ecological metadata
- **Audiovisual Core** — biodiversity media metadata
- **Camtrap DP** — camera trap data exchange
- **Movebank data model** — animal movement / biologging structure
- **OGC SensorThings API** — sensor and observation APIs
- **STAC** — geospatial asset metadata and discovery
- **OGC API - Features** — modern geospatial web APIs
- **GeoPackage** — portable field-friendly geospatial packaging
- **GeoParquet** — modern analytical geospatial format
- **Cloud Optimized GeoTIFF** — cloud-native raster distribution

See [`interoperability-and-standards.md`](interoperability-and-standards.md).

---

## Gaps worth paying attention to

The field still has recurring structural weaknesses:

- fragmented data models and weak interoperability
- too much dependence on expert validation bottlenecks
- donor-funded tools with thin long-term maintenance models
- interfaces that remain hard for frontline users
- poor integration across planning, monitoring, and operations
- strong innovation in sensors, but weaker downstream workflow design
- clearer standards for bioacoustics, restoration outcomes, and event messaging

Those gaps are also where the next serious generation of conservation technology is likely to emerge.

## See also

- [`docs/domain-slices.md`](domain-slices.md) — tighter taxonomy by problem space
- [`docs/gaps-and-opportunities.md`](gaps-and-opportunities.md) — deeper look at ecosystem gaps
