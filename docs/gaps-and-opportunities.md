# Gaps and Opportunities

This file focuses on the structural weaknesses in the conservation technology ecosystem and the opportunities they create for new work.

The point is not to complain. The point is to highlight where the field is still thin, so builders, funders, and contributors can focus their energy productively.

## Current structural gaps

### Weak interoperability in key domains

- **Camera traps**: Exchange between platforms is improving (Camtrap DP), but many deployments still use private formats. Integration with biodiversity publication systems remains inconsistent.
- **Passive acoustic monitoring**: No dominant exchange package comparable to Camtrap DP. Raw recordings and derived detections are often separated poorly. Metadata about deployment, habitat, effort, and calibration varies widely.
- **Restoration reporting**: Outcome schemas are weakly standardized. Definitions of success mix site, parcel, plot, intervention, and project-level metrics in ways that make comparison hard.
- **Real-time alerts and event messaging**: No common cross-platform format for incidents, patrols, alerts, and observations. Operational urgency often leads to brittle custom integrations.
- **Offline-first synchronization**: Low-bandwidth field deployments lack repeatable patterns for syncing data, media, and events when connectivity is intermittent.

### Operational and workflow bottlenecks

- **Expert validation bottlenecks**: Many systems rely on scarce expert time for QA, taxonomic review, or model validation. This limits scale.
- **Maintenance models**: Donor-funded tools often have thin long-term support. Open-source projects struggle with sustainability.
- **User interfaces**: Frontline users (rangers, field teams) often face interfaces that are hard to use in low-resource settings.
- **Data portability**: Teams can collect data, but moving it cleanly between field apps, databases, imagery pipelines, GIS tools, dashboards, and reporting systems remains hard.
- **Integration across planning, monitoring, and operations**: Systems for planning, monitoring, and operations often stay siloed.

### Technical and infrastructural weaknesses

- **Edge AI in rugged environments**: Low power, intermittent connectivity, ruggedization, local inference, privacy/security concerns, and sparse technical support.
- **Sensor metadata consistency**: In low-resource deployments, sensor metadata is often inconsistent or lost.
- **Model reproducibility**: Derived detections (from images, audio) are hard to trace back to source artifacts, models, and parameters.
- **Marine and fisheries data silos**: Operational and biodiversity pipelines often stay disconnected, even when technically interoperable.

## Opportunities for builders and contributors

These gaps are also where the next generation of conservation technology is likely to emerge. Here are some high-leverage areas.

### Build better exchange layers

- **Camera trap interoperability tools**: Validators, converters, and bridges between Camtrap DP and other formats. Focus on mappings to Darwin Core for publication.
- **Acoustic data packaging**: Develop a practical exchange package for PAM data, building on Audiovisual Core and biodiversity publication pathways.
- **Event message standards**: Propose and prototype shared schemas for conservation alerts, incidents, and observations. Start with OGC SensorThings API or similar.
- **Offline sync frameworks**: Open-source libraries or patterns for reliable data sync in low-bandwidth environments. Include media compression and prioritization.

### Strengthen operational workflows

- **Automated QA and validation**: Tools that reduce reliance on expert bottlenecks, such as community-driven validation workflows or semi-supervised models.
- **User-friendly field interfaces**: Mobile apps and dashboards designed for non-technical users in remote settings. Prioritize offline-first design.
- **Maintenance and sustainability models**: Frameworks for open-source conservation tools to achieve long-term viability, such as community governance or funding models.

### Advance domain-specific tooling

- **Restoration data models**: Schemas that cleanly carry interventions, outcomes, uncertainty, and provenance. Align with geospatial and biodiversity standards.
- **Edge AI toolkits**: Open hardware and software stacks for low-power wildlife detection, with remote management and update capabilities.
- **Marine integration bridges**: Tools that connect vessel monitoring, remote sensing, and biodiversity data in marine protected areas.

### Improve ecosystem infrastructure

- **Open data pipelines**: Better tooling for publishing to GBIF, OBIS, Movebank, and related archives. Include metadata enrichment and validation.
- **Geospatial asset management**: STAC-based catalogs and tools for conservation imagery, with offline support.
- **Community and collaboration platforms**: Tools that help conservation teams coordinate across organizations, share data securely, and track impact.

## Areas needing more attention

### Under-served domains

- **Marine conservation**: More tooling for fisheries transparency, marine mammal monitoring, and reef analysis beyond the current platforms.
- **Restoration and climate-biodiversity overlap**: Tools that link restoration outcomes to climate goals, carbon markets, and biodiversity metrics.
- **Urban and peri-urban conservation**: Technology for city-based conservation efforts, citizen engagement, and green infrastructure monitoring.
- **Indigenous and community-led monitoring**: Platforms that support traditional knowledge integration, participatory governance, and equitable data sharing.

### Cross-cutting needs

- **Ethics and equity**: Tools and frameworks for responsible AI, data sovereignty, and inclusive conservation technology development.
- **Capacity building**: Training resources, documentation, and mentorship programs for conservation practitioners to adopt and adapt technology.
- **Impact measurement**: Standardized ways to measure and communicate the real-world impact of conservation technology deployments.

## How to get started

If you are a builder or contributor:

1. **Start with user needs**: Talk to conservation practitioners. What breaks in their workflows? What data do they struggle to move?
2. **Align with standards**: Use existing interoperability layers where possible. Do not invent new data models without checking TDWG, OGC, and domain-specific efforts.
3. **Prioritize portability**: Design so your outputs can be used by others without your UI. Support export to common formats early.
4. **Consider sustainability**: Think about maintenance, documentation, and community from the start.
5. **Engage the ecosystem**: Join WILDLABS, contribute to open-source repos, and participate in challenges or awards.

Funders and organizations can help by:

- Supporting interoperability efforts and standards development.
- Funding maintenance and long-term support for open-source tools.
- Creating prizes or challenges that reward practical integration and data portability.

This is not an exhaustive list. It is a map of where the ecosystem feels thin enough that new work could have outsized impact.

## See also

- [`docs/interoperability-and-standards.md`](interoperability-and-standards.md) — standards to build on
- [`docs/communities-funding-and-events.md`](communities-funding-and-events.md) — communities and funding for these opportunities