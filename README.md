# SGP Sample Context Template

## Overview

The SGP context template is used to gather geological, geographical and sample-specific information, related to samples that have geochemical data for import into the SGP database. Details of geochemical data and geochemical methods are dealt with separately.

Where possible we ask that collaborators provide this context information, as they are often able to provide important details that are not available in published papers.

Details can be provided for samples from **one or more sites** in one template file.

The information in the template could apply to one published study, but it can also be used to provide details for samples and sites that appear across multiple related publications, or where associated geochemical data is unpublished but provided to the SGP database.

On ingestion, samples are grouped together into projects, based on publications or broader research themes. On a more granular level, individual geochemical measurements are directly associated with the publication where they first appear.

---

## Template Structure

The template has five visible tabs

- User Guide
- Sites
- Samples
- PrepMethod
- Dictionary of Sed Structures

The primary tabs for data entry are **Sites** and **Samples**.

---

### Sites

In SGP we are primarily dealing with single measured outcrop sections or cores.

Sites are primarily defined by their geography. Each site has one set of coordinates - we don't currently accomodate more complex geometries such as lines or polygons.

Samples can be collected from the same site at different times by different people (different collecting events).

#### section_name

The name of the outcrop or the core.

**Core** names are usually formalized when the core is made - use the name as recorded by the core storage facility, or core creator.

For **outcrops**, if published, use the name as reported in the paper, and corresponding to any figures or tables. (If the same site has been given different names in different papers, please provide that information in the notes field at the end of the sheet - "alternative site names" can be recorded in the database).

Site names in SGP are not required to be unique - by necessity to accommodate legacy data - but it is preferable if they are. We recommend that sites are given names that are short, alphanumeric, with minimal separators, and distinctive in the context of a global database (i.e., not simply "Locality 1" or "Section A"). Avoid mixing 1 (one) and the letters i and l, and similarly 0 (zero) and the letter o. Using names or abbreviations based on local geography (a creek, a quarry etc.) can be helpful, but bear in mind the scale of the feature and uniqueness of the name, and consider whether someone could easily give the same name to a different collecting point in that region. To give some extreme examples: in the United States it would be best not to simply use "Mississippi River" (very long!) or "Mill Creek" (there are thousands of them!). Adding a short project-specific code or number could be useful in such cases.

If a new collection is undertaken in the same area but from a different stratigraphic baseline, give that site a new name and a new set of coordinates, measured from the new baseline.

**Examples:**

- Lönstorp-1
- S1409
- Tattenhoe
- Surprise Creek 2

#### site_type

Dropdown. Sites in SGP are primarily divided into "core" or "outcrop". Marine cores are cores from the modern ocean.

**Examples:**

- core
- outcrop
- marine_core

#### country

ISO country names - use the ISO [English Short name](https://www.iso.org/obp/ui/#search)

**Examples:**

- United States
- Canada
- Australia

#### state_province

The name of the next smaller adminstrative region within a country. Darwin Core term [stateProvince](http://rs.tdwg.org/dwc/terms/stateProvince)

**Examples:**

- Colorado
- Guizhou
- Northwest Territories

#### county

The name of the next smaller adminstrative region within a state or province. Darwin Core term [county](http://rs.tdwg.org/dwc/terms/county)

**Examples:**

- Lancashire
- White Pine
- Anshan

#### site description

A description of the site, primarily geographic but with any other details that could be used to refine the location. This description is particulary useful when comparing similar sites, and for verification of latitude and longitude values. See Darwin Core term [Locality](https://dwc.tdwg.org/list/#dwc_locality:~:text=http%3A//rs.tdwg.org/dwc/terms/locality).

**Examples:**

- approx. 3 km to the northeast of Coppercap Mountain in the Mackenzie Mountains
- Trench by the river, near Conego Marinho (30km from Januária)
- Outcrop on north side of Highway 6, ~12 km northwest of Eureka,NV

#### latitude

Verbatim latitude of the site. Decimal degrees are preferred, but the original recorded format is also acceptable. (The database stores the original version, as well as the decimal latitude version). See Darwin Core term [verbatimLatitude](http://rs.tdwg.org/dwc/terms/verbatimLatitude).

**Examples:**

- 41.74167
- 53°52'13.4"N
- 20°50.3467'S

#### longitude

Verbatim longitude of the site. Decimal degrees are preferred, but the original recorded format is also acceptable. (The database stores the original version, as well as the decimal longitude version). See Darwin Core term [verbatimLongitude](http://rs.tdwg.org/dwc/terms/verbatimLongitude).

**Examples:**

- -105.85361
- 122°30'44.5"W
- 118°21.515'E

#### datum

The geodetic datum that applies to the provided latitude and longitude. See Darwin Core term [verbatimSRS](http://rs.tdwg.org/dwc/terms/verbatimSRS). Coordinates taken from Google Maps will have the geodetic datum of WGS84.

**Examples:**

- WGS84
- NAD27
- GDA94

#### elevation (m)

The elevation in meters of the site.

**Examples:**

- 1472.18

#### craton_terrane

The craton or terrane that the site is part of.

**Examples:**

- Laurentia
- Avalonia
- North China

#### basin name

The name of the sedimentary basin that the site is part of.

**Examples:**

- Taconic Foreland Basin
- Borden Basin
- Vindhyan Basin
- Bambuí Basin

#### basin type

Dropdown. The type of sedimentary basin.

**Examples:**

- rift
- foreland - peripheral
- intracratonic sag

#### metamorphic_bin

Dropdown. Sites are sorted into three low-grade metamorphic bins, roughly based on metapelite zones as follows:

1. Diagenetic zone. Under mature, preserved biomarkers, KI>0.42, CAI ≤3, Ro <2.0, facies: zeolite-subgreenschist facies, grade: diagenesis-very low grade

2. Anchizone. Over-mature, no preserved biomarkers, CAI=4, Ro 2-4, facies: sub-greenschist, grade: very low grade

3. Epizone. Ro>4, CAI=5, KI<0.25, facies: greenschist, grade: low-grade

**Examples:**

- Diagenetic zone
- Anchizone
- Epizone

#### collection start date

The date when collecting started at this particular site for these particular samples. Ideally YYYY-MM-DD, if known, but lower resolution or verbatim collecting dates are also accepted (e.g. Summer 2009)

**Examples:**

- 2021-04-01
- October 2008

#### collection end date

The date when collecting ended at this particular site for these particular samples. Ideally YYYY-MM-DD, if known, but lower resolution or verbatim collecting dates are also accepted (e.g. Summer 2009)

**Examples:**

- 2009-10-14
- December 2008

#### collectors

List of collectors, in order if order is significant i.e. lead/primary collector first. Use full names and separate multiple collectors with commas.

**Examples:**

- Julie Dumoulin, John Slack
- Robert Gaines

#### collection reason

A brief description of the motivation for collection.

**Examples:**

- long-duration Earth history study
- black shale geochemistry study (paleo-redox and paleo-salinity)
- petroleum geology
- chemostratigraphy through the Orosirian Period
- redox chemistry, metal exploration

#### notes

Any significant details that were not captured in the preceding columns. This could include notes about the section name, related sites, details of how coordinates were determined, or any other information that would provide valuable additonal context for this particular site.

**Examples:**

- Little information is available on these cores. The lat/long were estimated from Fig. 1 of Nyhuis et al., 2014 based on the apparent river morphology and using Google Earth. Exact metamorphic grade not clear. Siedenberg et al. 2016 report this core has reached the gas window so it was coded as diagenetic zone, but it may be anchizone
- Lat-long from Yale Peabody Museum https://collections.peabody.yale.edu/search/Record/YPM-IP-533117
- Lat-long reported in Raiswell and Canfield 1998, see also Lamont-Doherty records.
- Site details taken from the footnote on table 3, Harris et al,. 2013

---

### Samples

In SGP we are primarily dealing with rock hand samples, which are subsequently powdered for bulk geochemical analyses. However, the database also accomodates sub-samples (e.g. for LA-ICP-MS data) with a link to a parent sample, and more specific sample types for targetted analyses e.g. "skeletal (foram)" for carbonate analysis.

#### parent sample number

Rarely used, but if the samples are sub-samples, especially if multiple "child" samples were measured from one parent, then give the name of the parent sample here. Note the parent sample must ALSO have a row in the template, or exist in the database already.

**Examples:**

- DB10
- F1003-0.2

#### original sample number

The name or number of the sample, as it is published - in particular corresponding to any associated data tables.

Tracking samples in SGP is a major challenge. We don't require that original sample names are unique - by necessity to accommodate legacy data - but it is preferable if they are. We recommend that samples are given names that are short, alphanumeric, with minimal and consistantly-used separators, and distinctive in the context of a global database (i.e., not simply "1, 2, 3, 4"). Avoid mixing 1 (one) and the letters i and l, and similarly 0 (zero) and the letter o. Keep the same format across papers. Avoid anything that that looks remotely like a date. Avoid using the height in the stratigraphic section or the depth in the core as the only sample identifier, although it could be combined with a short code relating to site name for example. Height/Depth values are stored separately, and slight variations in precision across tables can make it very difficult to track the same sample.
See [SGP Phase 2 wiki](https://github.com/sgp-docs/sgp_phase2/wiki/A.-Database-description#sample) for description of sample identifiers in SGP.

**Examples:**

- DB10
- S86A-901.8
- AK-SC-12

#### height in section/depth in core (m)

The stratigraphic height in the measured outcrop section, or the depth in the core. Numeric values only, in meters.

**Examples:**

- 10.5
- 101

#### sample type

Dropdown. Samples where a rock sample from a single stratigraphic level has been crushed or analyzed are represented as 'bulk (stratigraphic)' (this also includes most microdrilled samples, where multiple components (matrix/skeletal grains etc.) are likely to be incorporated). This is the most common sample type in SGP.

Multiple samples from a larger stratigraphic range which are crushed together are represented as 'bulk (chips, cuttings, composite)'.

If only a specific component of the rock is analyzed, that specific phase (e.g., pyrite or a bioclast like a brachiopod) should be selected.

**Examples:**

- bulk (stratigraphic)
-

#### Interpreted Age

#### Interpreted Age

## PrepMethod

PrepMethod is used to gather information about how samples were prepared - e.g. tungsten carbide shatterbox. This is one piece of geochemical methodology that we consider useful, which is very frequently left out of published papers method sections. The rest of the methodology can usually be coded by SGP from the paper.

## Ingestion

## Ingestion
