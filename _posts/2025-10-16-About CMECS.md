---
title: "About CMECS"
date: 2025-10-16
---
The Coastal and Marine Ecological Classification Standard (CMECS) Catalog is the authoritative collection of ecological units (terms + definitions) and unit relationships (the CMECS framework). 

The CMECS Catalog was originally created by [NatureServe](https://www.natureserve.org/products/coastal-and-marine-ecological-classification-standard-cmecs) as a Microsoft Access database, and represents the CMECS units as published in the [FGDC-STD-018-2012 document](https://repository.library.noaa.gov/view/noaa/27552). The contents of this database were exported into tables in Microsoft Excel Worksheets, checked for accuracy against the FGDC-STD-018-2012 document, then encoded in an Extensible Markup Language (XML) Resource Description Framework (RDF) and Web Ontology Language (OWL) file, cmecs.owl, and released as [CMECS v1.0.0](https://github.com/NOAA-OCM/cmecs/releases/tag/v1.0.0). 

The **CMECS Catalog** [cmecs.owl](https://github.com/NOAA-OCM/cmecs/tree/main/src) file the complete representation of the CMECS classification. It contains all units that are or have been members of the CMECS classification throughout its lifecycle, as well as various annotations that provide metadata for each unit that enable Findability, Accessibility, Interoperability, and Reuse (FAIR, https://www.go-fair.org/fair-principles/). The cmecs.owl file is stored and managed in a Git repository; authoritative versions are publicly released via this GitHub site as changes are made. Version releases also include the CMECS Catalog in CSV and XLXS formats. A browsable text output of the CMECS Catalog ecological units and implementation guidance, the [**CMECS Thesaurus**](https://github.com/NOAA-OCM/cmecs/wiki/CMECS-Thesaurus-Quick-Link), is also available in PDF and MD formats. 

See the [Files and Releases](https://github.com/NOAA-OCM/cmecs/wiki/CMECS-Catalog-Files-and-Releases-Links) page of this Wiki for a guide and links to these files.

**_NEW: The most recent version of the CMECS Catalog is available to browse on [EcoPortal](https://ecoportal.lifewatch.eu/ontologies/CMECS)_**

## About Versions and Releases

The CMECS Catalog follows many Semantic Versioning Specification (SemVer, [semver.org](https://semver.org/)) recommendations, which provide a clear strategy for managing and publishing the various types of incremental changes made over the Catalog's lifecycle. The CMECS Catalog uses a X.Y.Z number format for its versioning scheme to indicate Major (X), Minor (Y), and Patch (Z) changes as follows:
-  MAJOR versions are assigned for the first published release and for completely-reviewed and updated releases. For example,
    - Version 1.0.0 is the the representation of CMECS as published in the FGDC-STD-018-2012 document
    - Version 2.0.0, when released, will be the version that has undergone the first complete review of all settings, components, and modifiers, including editorial changes and guidance additions. This review is underway but not yet complete. 
    - Version 3.0.0 will be the version that has undergone a second complete review of all settings, components, and modifiers, including editorial changes and guidance additions. This review cycle will not be initiated for several years.
- MINOR versions are assigned for releases that include changes to one or many units, unit additions and deprecations, or changes to the CMECS framework. These changes can be adopted and released at any time and do not have to conform to any specific cycle, but efforts will be made to compile incremental changes into as few releases as possible. For example,
    - 1.1.0 will be the release that includes changes to Substrate Component units and hierarchy, unit additions, unit deprecations, and added annotations.
    - 1.2.0 will be the release that includes changes to Biotic Component units and hierarchy, unit additions, unit deprecations, and added annotations.
    - 1.3.0 will be the release that includes changes to Geoform Component units and hierarchy, unit additions, unit deprecations, and added annotations.
- PATCH versions are assigned for releases that include editorial corrections, new or revised guidance or other annotation information but DO NOT include changes to units or hierarchy. For example,
     - 2.0.1 would be assigned to a release that includes only editorial corrections or new annotations, etc.

## About Unit Status and Types of Changes 

CMECS units may undergo various types of changes from version to version. Listed below are the unit status and the types of changes that may occur. Each original CMECS unit is assigned a unique Unit Identifier (CMECS_XXXXXXXX). Certain types of changes require issuance of a new Unit ID or a Unit ID deprecation. Units retain their Unit IDs until they are modified in a way that alters the fundamental meaning, or concept, of the unit. When units are deprecated, they are removed from the CMECS classification but remain members of the CMECS Catalog so that they can be referenced by works that have used earlier versions. 
  
### Unit Status
- **Original Unit** A unit that has been added to the CMECS Catalog for the first time at any point in the Catalog's life-cycle. All units published in the FGDC-STD-018-2012 document are considered Original Units until they are modified in a way that alters the fundamental meaning, or concept, of the unit. Units that are added to the Catalog in subsequent versions are considered Original Units if they represent new concepts and are not the result of lumping, splitting, or other re-definition of a predecessor unit's concept. 
- **Deprecated Unit** A unit that has been removed from the CMECS classification as a result of a significant change in concept that does not produce a Derived Unit.  Deprecated Units remain in the CMECS Catalog so that they can be referenced by works that have used earlier versions. 
- **Derived Unit** A unit that originates as the result of lumping or splitting existing (predecessor) units, or changing levels up or down, or moving laterally in the hierarchy.

### Types of Change
- **Addition** An Original Unit is added to the CMECS classification and Catalog and is assigned a unique Unit Code.
- **Deprecation** A unit is removed from the CMECS classification, but remains a member of the CMECS Catalog along with its Unit Code.
- **Split** A single unit is divided into multiple new units as the result of a conceptual change to the predecessor unit. The Unit ID of the predecessor unit may be retained by one of the derived units; unique Unit IDs may also be assigned to additional derived units. 
- **Lump** Multiple predecessor units are combined into a single unit, which represents a new or modified concept within the CMECS classification. The Unit ID of one of the predecessor units may be retained by the derived unit, or all predecessor Unit IDs may be deprecated and a new Unit ID assigned to the derived unit.
- **Complex Split/Lump** Multiple predecessor units are both split and lumped as the result of conceptual changes to form multiple new units. Unique Unit IDs may be assigned or deprecated.
- **Change in Level** A type of membership change where a unit is moved either up or down from one level of the hierarchy to another as necessitated by conceptual changes to other units. No change to the Unit ID is necessary.
- **Membership Change** A unit moves laterally within the hierarchy, but does not change conceptually  (e.g., a biotic community moves from one biotic group to another.) No change to the Unit ID is necessary.
- **Name Change** The name of the unit is changed. This includes changes to accommodate prevailing usage (eg. starfish becomes seastar), but not corrections to typographical errors. No change to the Unit ID is necessary.
- **Attribute Change** Addition of new attributes and content changes or corrections to any other attribute of the unit (e.g., adding new implementation guidance, references.) No change to the Unit ID is necessary.
- **Editorial Change** Changes that correct typographic errors and grammar, or that clarify existing text. No change to the Unit ID is necessary.
