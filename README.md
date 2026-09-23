# SGP Sample Context Template

## Overview

The SGP context template is used to gather geological, geographical, and sample-specific information, related to samples that have geochemical data for import into the SGP database. Details of geochemical data and geochemical methods are dealt with separately.

Details can be provided for samples from **one or more sites** in one template file.

The information in the template could apply to one published study, but it can also be used to provide details for samples and sites that appear across multiple related publications, or where associated geochemical data is unpublished but provided to the SGP database.

On ingestion, samples are grouped together into projects, based on publications or broader research themes. On a more granular level, individual geochemical measurements are directly associated with the publication where they first appear.

---

## Template Structure

The template has five visible tabs:

- User Guide
- Sites
- Samples
- PrepMethod
- Dictionary of Sed Structures

The **User Guide** provides information about how to fill the template - it is an abbreviated version of this document.

The main sheets for data entry are **Sites** and **Samples**. Columns for these are described in the sections below, with real examples taken from the SGP database. Some are based on controlled vocabularies (dictionaries) and values must be chosen from a dropdown list (these are indicated as "Dropdown" in the descriptions below).

The **PrepMethod** is used to collect information about how samples are prepared for analysis.

The **Dictionary of Sed Structures** is a dictionary list for sedimentary structures for reference - more than one sedimentary structure can be associated with a single sample and therefore these terms are not provided as a dropdown list.

Hidden tabs include the other dictionaries used in dropdowns.

---

### Sites

In SGP we are usually dealing with single measured outcrop sections or cores.

Sites are primarily defined by their geography. Each site has one set of coordinates (we don't currently accommodate more complex geometries such as lines or polygons).

Samples can be collected from the same site at different times by different people (different collecting events).

#### section name

The name of the outcrop or the core.

**Core** names are usually formalized when the core is made - use the name as recorded by the core storage facility, or core creator.

For **outcrops** use the name as reported in any published paper, in particular corresponding to any figures or tables. (If the same site has been given different names in different papers, please provide that information in the notes field at the end of the sheet - "alternative site names" can be recorded in the database).

If a new collection is undertaken in the same area but from a different stratigraphic baseline, give that site a new name and a new set of coordinates, measured from the new baseline.

**Examples:**

- Lönstorp-1
- S1409
- Tattenhoe
- Surprise Creek 2

#### site type

_Dictionary/Dropdown_

Sites in SGP are primarily divided into "core" or "outcrop". Marine cores are cores from the modern ocean.

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

#### state or province

The name of the next smaller administrative region within a country. Darwin Core term [stateProvince](http://rs.tdwg.org/dwc/terms/stateProvince)

**Examples:**

- Colorado
- Guizhou
- Northwest Territories

#### county

The name of the next smaller administrative region within a state or province. Darwin Core term [county](http://rs.tdwg.org/dwc/terms/county)

**Examples:**

- Lancashire
- White Pine
- Anshan

#### site description

A description of the site, primarily geographic but with any other details that could be used to refine the location. This description is particularly useful when comparing similar sites, and for verification of latitude and longitude values. See Darwin Core term [Locality](http://rs.tdwg.org/dwc/terms/locality).

**Examples:**

- approx. 3 km to the northeast of Coppercap Mountain in the Mackenzie Mountains
- Trench by the river, near Conego Marinho (30km from Januária)
- Outcrop on north side of Highway 6, ~12 km northwest of Eureka,NV

#### latitude

Verbatim latitude of the site. Decimal degrees are preferred, but any correctly formatted original version is also acceptable (e.g. degrees, minutes, seconds or decimal minutes). See Darwin Core term [verbatimLatitude](http://rs.tdwg.org/dwc/terms/verbatimLatitude).

**Examples:**

- 41.74167
- 53°52'13.4"N
- 20°50.3467'S

#### longitude

Verbatim longitude of the site. Decimal degrees are preferred, but any correctly formatted original version is also acceptable (e.g. degrees, minutes, seconds or decimal minutes). See Darwin Core term [verbatimLongitude](http://rs.tdwg.org/dwc/terms/verbatimLongitude).

**Examples:**

- -105.85361
- 122°30'44.5"W
- 118°21.515'E

#### datum

The geodetic datum that applies to the provided latitude and longitude. See Darwin Core term [verbatimSRS](http://rs.tdwg.org/dwc/terms/verbatimSRS). For coordinates taken from Google Maps use the geodetic datum of WGS84.

**Examples:**

- WGS84
- NAD27
- GDA94

#### elevation (m)

The elevation in meters of the site, if available.

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

_Dictionary/Dropdown_

The type of sedimentary basin.

**Examples:**

- rift
- foreland - peripheral
- intracratonic sag

#### metamorphic bin

_Dictionary/Dropdown_

Sites are sorted into three low-grade metamorphic bins, roughly based on metapelite zones as follows:

1. Diagenetic zone. Under mature, preserved biomarkers, KI>0.42, CAI ≤3, Ro <2.0, facies: zeolite-subgreenschist facies, grade: diagenesis-very low grade

2. Anchizone. Over-mature, no preserved biomarkers, CAI=4, Ro 2-4, facies: sub-greenschist, grade: very low grade

3. Epizone. Ro>4, CAI=5, KI<0.25, facies: greenschist, grade: low-grade

**Examples:**

- Diagenetic zone
- Anchizone
- Epizone

#### collection start date

The date when collecting started at this particular site for these particular samples. Ideally YYYY-MM-DD, if known, but lower resolution or verbatim collecting dates are also accepted (e.g. Summer 2009).

**Examples:**

- 2021-04-01
- 2010
- October 2008

#### collection end date

The date when collecting ended at this particular site for these particular samples. Ideally YYYY-MM-DD, if known, but lower resolution or verbatim collecting dates are also accepted (e.g. Summer 2009).

**Examples:**

- 2009-10-14
- December 2008

#### collectors

List of collectors, in order if order is significant i.e. lead/primary collector first. Use **full names** without titles, and separate multiple collectors with commas.

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

Any significant details that were not captured in the preceding columns. This could include notes about the name, related sites, details of how coordinates were determined, or any other information that would provide valuable additional context for this particular site.

**Examples:**

- Little information is available on these cores. The lat/long were estimated from Fig. 1 of Nyhuis et al., 2014 based on the apparent river morphology and using Google Earth. Exact metamorphic grade not clear. Siedenberg et al. 2016 report this core has reached the gas window so it was coded as diagenetic zone, but it may be anchizone
- Lat-long from Yale Peabody Museum https://collections.peabody.yale.edu/search/Record/YPM-IP-533117
- Lat-long reported in Raiswell and Canfield 1998, see also Lamont-Doherty records.
- Site details taken from the footnote on table 3, Harris et al,. 2013

---

### Samples

In SGP we are primarily dealing with rock hand samples, which are subsequently powdered for bulk geochemical analyses. However, the database also accommodates sub-samples (e.g. for LA-ICP-MS data) with a link to a parent sample, and more specific sample types for targeted analyses e.g. "skeletal (foram)" for carbonate analysis.

#### parent sample number

Rarely used, but if the samples are sub-samples, especially if multiple "child" samples were measured from one parent, then give the name of the parent sample here. Note the parent sample must ALSO have a row in the template, or exist in the database already.

**Examples:**

- DB10
- F1003-0.2

#### original sample number

The name or number of the sample, as it is published - in particular corresponding exactly to any associated data tables.

**Examples:**

- DB10
- S86A-901.8
- AK-SC-12

#### height in section/depth in core (m)

The stratigraphic height in the measured outcrop section, or the depth in the core. Numeric values only, in meters.

**Examples:**

- 10.5
- 101

#### section name

_Dropdown_

The name exactly as reported on the Sites sheet (the dropdown on this column is not based on a dictionary, but rather links to the section name column on the Sites tab. Cells will turn red if the name does not exactly match).

**Examples:**

- Lönstorp-1
- S1409
- Tattenhoe
- Surprise Creek 2

#### sample type

_Dictionary/Dropdown_

The most common sample type in SGP is 'bulk (stratigraphic)'. This category represents rock samples from single stratigraphic level, crushed and powdered for analysis. The category also includes most microdrilled samples, where multiple components (matrix/skeletal grains etc.) are likely to be incorporated into any analyses.

By contrast, multiple samples from a larger stratigraphic range which are crushed together for analysis are represented as 'bulk (chips, cuttings, composite)'.

If only a specific component of the rock is targetted for analysis, then more precise sample types apply (e.g., mineral (pyrite) or skeletal (brachiopod)).

**Examples:**

- bulk (stratigraphic)
- skeletal (foram)
- matrix (micrite)

#### geological unit name

The lithostratigraphic unit name, at the highest resolution known. Ideally provide the formal stratigraphic name, without abbreviations (e.g. Formation, and not Fm or Fm.). National Geological Surveys are often the best source for accepted names. Some commonly used resources in SGP are:

- [Macrostrat Lexicon](https://dev.macrostrat.org/lex/strat-names)
- [Geolex - USGS National Geologic Map Database](https://ngmdb.usgs.gov/Geolex/search)
- [Weblex Canada](https://weblex.canada.ca/weblexnet4/weblex_e.aspx)
- [British Geological Survey Lexicon](https://webapps.bgs.ac.uk/lexicon/home.cfm)
- [Australian Stratigraphic Units Database](https://asud.ga.gov.au/search-stratigraphic-units)
- [China Lexicon of Stratigraphic Names](https://chinalex.geolex.org/)
- [International Geology Website and Database](https://geolex.org/)

It is also possible to provide a "verbatim" geological unit name, which includes additional detail, if the formal names are not sufficient - for example, to specify a relative but informal position within the unit such as 'lower Frankfort Formation', or to give a hierarchical list such as 'Colorado Group, Belle Fourche Formation'. The latter is especially helpful if, for example, a formation name can be included in different groups depending on geography. In the database the sample will be associated with a formal name, but these more detailed versions will be kept alongside as "verbatim_strat".

**Examples:**

- Baiguridji Formation
- Bantry Shale Member
- La Ciénega Formation, Unit 3

#### depositional environment bin

_Dictionary/Dropdown_

Environments are divided into three primary bins - inner shelf (marine), outer shelf (marine) and basinal (marine) - in addition to lacustrine, fluvial and estuarine. The first three bins are defined based on Sperling et al. 2015:

1. Inner Shelf: Sample interbedded with abundant shallow-water
   indicators. This includes clastic beds with wave-generated sedimentary
   structures as well as shallow-water carbonates such as stromatolites, oolites,
   and rip-up conglomerates. Evidence of exposure—i.e. mudcracks, karsting,
   teepee structures—are often in relatively close stratigraphic proximity on the
   meters to 10s of meters scale.

2. Outer Shelf: Sample from sequences that generally show little
   wave activity, but with occasional evidence for storm and/or wave activity,
   such as hummocky cross-stratified sands encased in shales. Evidence for
   exposure is not in close stratigraphic proximity.

3. Basinal: Sample from successions with no evidence for any storm
   and/or wave activity for an appreciable (i.e. >50 m) stratigraphic distance.
   Generally located considerably basin-ward of shallower-water facies.

**Examples:**

- inner shelf (marine)
- outer shelf (marine)
- basinal (marine)
- lacustrine
- fluvial
- estuarine

#### depositional environment detail

A more detailed category of depositional environment (added 2021). This list of terms is from [Macrostrat Environments Lexicon](https://dev.macrostrat.org/lex/environments). The dropdown lists carbonate marine depositional environments, siliciclastic marine depositional environments, followed by fluvial, lacustrine, glacial, and other depositional environments. This dictionary is particularly useful for providing a more refined interpretation of carbonate settings.

**Examples:**

- deep subtidal ramp (carbonate)
- offshore shelf (carbonate)
- submarine fan (siliciclastic)

#### depositional environment description

A free-text description of the depositional environment, as nuanced or detailed as you see fit e.g. 'deposition below storm wave base on a broad, shallow, sloping shelf in the absence of persistent infauna'.

**Examples:**

- Shallow marine upper shoreface. Late stage siliciclastic infill of the Zaris sub-basin.
- Distally-steepened, storm-dominated carbonate ramp
- passive continental margin, below wave base, separated from the coast by a carbonate barrier

#### is_turbiditic (t/f)

_Validated_

Whether conditions were turbiditic. This should reflect the broad stratigraphic package, even if the sample itself is a shale deposited from hemipelagic suspension (i.e. the Te unit). This column will only allow 't' or 'f'.

**Examples:**

- t
- f

#### biostratigraphy

The biostratigraphic zone. (see Zone and Subzone within the [Macrostrat Intervals lexicon](https://dev.macrostrat.org/lex/intervals) - e.g. [Aulacostephanus eudoxus](https://dev.macrostrat.org/lex/intervals/841)).

**Examples:**

- Streptognathodus gracilis zone
- Aulacostephanus eudoxus zone

#### geological age

[International age name](www.stratigraphy.org), at the finest level possible.

**Examples:**

- Ordovician
- Aptian

#### lithology

_Dictionary/Dropdown_

A restricted version of [Macrostrat Lithology Lexicon](https://dev.macrostrat.org/lex/lithologies) - focused on sedimentary rocks, and, for example, using the Dunham scheme only for carbonates.

**Examples:**

- Shale
- Sandstone
- Grainstone

#### lithological texture (modifier)

_Dictionary/Dropdown_

This is used to add a textural modifier to the base lithology. It should ONLY be used if it adds additional information, not to repeat the lithology (e.g., no need for "silty silstones").

**Examples:**

- Silty
- Muddy
- Clayey
- Sandy

#### lithological composition (modifier)

_Dictionary/Dropdown_

This is used to add a compositional modifier to the base lithology. It should ONLY be used if it adds additional information, not to repeat the lithology (e.g., no need for "phosphatic phosphorites").

**Examples:**

- calcareous
- siliceous
- carbonaceous
- pyritiferous
- micaceous
- phosphatic
- dolomitic

#### color

Ideally a **single** color (black, grey, green), although modifiers are allowed, in which case, preferably use Munsell-style names e.g., Moderate reddish brown, Medium grey, Greyish black.

**Examples:**

- black
- dark grey
- medium light grey
- blackish brown

#### is_bioturbated (t/f)

_Validated_

Whether or not the sample was burrowed, to any extent. This column will only allow 't' or 'f'.

**Examples:**

- t
- f

#### fossils

Any fossils associated with the sample, to the highest level of identification available. Use a comma-separated list for multiple fossil types.

**Examples:**

- graptolites, brachiopods, bivalves
- Leiosphaeridia crassa
- sponge spicules
- Triarthrus eatoni

#### sedimentary structures

_Dictionary_

Any sedimentary structures associated with the sample - e.g. cross laminations, grading. The dictionary of sedimentary structures in the final tab should be used for reference. Please use terms exactly as reported, and use a comma-separated list for multiple sedimentary structures (A dropdown is not provided, since more than one term can apply to a single sample). (The dictionary was initially populated with some terms from [Macrostrat lexicon of lithology attributes](https://dev.macrostrat.org/lex/lith-atts)).

**Examples:**

- cross laminations
- load casts
- graded-normal

#### lithological notes

Any notes about the lithology e.g., a more detailed description if you feel that the dictionary table values do not adequately describe the samples, or details of how the lithology was determined.

**Examples:**

- occasional small pyrite lags and/or phosphatic nodules (1-2mm)
- Unknown if specific sample is bioturbated, but bioturbation and reworking common in column. Lithologies were determined using carbonate percent measurements from Marz et al., 2016. Samples considered limestone (CaCO3 > 80%) were labeled wackestone or lime mudstone based on strat columns in Ali Hussein et al., 2014. Many samples were considered marl in the strat column of Ali Hussein et al., 2014 but the carbonate percentage is considered a more accurate discriminator of lithology. Note there are many silicified beds and this is not well captured by the lithology coding.

#### interpreted age (Ma)

An estimate for the age of the sample in millions of years. **Numerical value only** with no modifiers or symbols (no age ranges, no < or >)

- 560
- 496.76

#### interpreted age justification

Justification for the interpreted age provided. Ages can be interpreted to various levels of detail. For instance, the estimate can be based on an assumed sedimentation rate + linear interpolation, or groups of samples can be assigned an age based on proximity to a time marker (ash bed etc.). It is fine to note uncertainty or possible issues with the assignment, which could come in useful for refinements/updates at a later date.

**Examples:**

- Frasnian-Famennian boundary estimated at 475 meters in State Chester core--372.2 Ma in ICS chart 1/27/2016. Ages estimated above and below based on 50 kyr/m average shale depositional rate.
- This formation is likely Middle Ordovician, and all samples are given an age of 465 Ma.
- Tapley Hill Fm. records post-glacial (Sturtian) deposition (Preiss, 2000; Preiss et al., 2011) and is conservatively between 660–640 Ma. Interpreted age is taken from the Re-Os age of 645 +- 4.8 Ma on lower strata of the Tapley Hill Fm. from the Blinman-2 core (Kendal et al., 2006).
- There are no good age constraints on the Papoose Creek Formation. Sample was given an age of 615 Ma based on the correlation figure of Macdonald et al., 2023

#### maximum age

An estimate for the maximum age of the sample in millions of years. **Numerical value only** with no modifiers or symbols (no age ranges, no < or >)

**Examples:**

- 343.50
- 423

#### minimum age

An estimate for the minimum age of the sample in millions of years. **Numerical value only** with no modifiers or symbols (no age ranges, no < or >)

**Examples:**

- 355
- 419.20

#### sample storage location

The place where the physical sample is stored.

**Examples:**

- Department of Earth and Planetary Sciences, Yale University
- British Geological Survey

#### contact person for sample

The person responsible for the physical samples. Full name.

**Examples:**

- Erik Sperling
- Rachel Wood

#### notes

Any clarifications or comments about the sample - details that may not have been adequetly covered by the columns provided, or very specific to a particular study.

**Examples:**

- Original sample number from A. Knoll notebook. HU= Harvard University number.
- Biostratigraphy extrapolated from nearby cores. See Remírez et al. (2023) for more details.
- < 15m below interval of bedded massive sulphides

## PrepMethod

PrepMethod records information about how a sample was prepared for analysis, such as grinding in a tungsten carbide shatterbox or an agate mortar. We collect this information here because sample preparation is an important part of the analytical methodology, but it is frequently omitted from published methods sections.

In most cases, a single preparation method will have been used for all analyses of a set of samples. In this case, simply provide the preparation method once. However, different preparation methods may sometimes be used for different analyses, for example if analyses were carried out in different laboratories. This is why PrepMethod is not a single column on the sample tab: a sample may have more than one preparation method associated with its analytical data.

Where different preparation methods were used, specify which preparation method applies to each set of associated analytical data. For example, you might indicate that tungsten carbide was used for all elemental analyses, while agate mortar was used for carbon isotope analyses.
