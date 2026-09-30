# SGP Naming Guide

Tracking samples and sites across projects and publications is one of the major challenges in SGP.

Where available, we encourage the use of standardized identifiers such as the **International Generic Sample Number (IGSN)**. SGP can store IGSNs alongside other identifiers.

However, in practice researchers will continue to create local names during field work and in the lab, and many existing datasets contain only these names.

Taking care with local naming systems from the start can go a long way to help. The aim is create names that are **distinctive, readable, consistent, and robust when datasets are shared and combined**. There is no single naming system that will work for every project, but some general guidelines apply.

In particular, consider whether your names could be confused with names already used for the same site, section, or region. A name that is unique within one field notebook may not remain unique when combined with another dataset.

For example, SGP contains two sets of samples with the prefix **LBZ**, from `Longbizui` but collected on different dates, by different collectors, and from different stratigraphic baselines. SGP therefore has two different samples called `LBZ-100`, and their associated metadata are sufficiently similar (same formation, same age bin, same lithology) that the names could easily cause confusion.

In another example, SGP also contains two sets using the prefix **DL**: one derived from Dob's Linn and one from the collector David Loydell. However, in this case, the associated sample metadata are distinct, so the shared prefix is less problematic.

## General Recommendations

- **Avoid overly simple identifiers.** Do not use names such as `1`, `2`, `3`, `Section 1`, or `Locality A` (SGP has nineteen samples called '1'!)
- **Avoid easily confused characters.** In particular, be careful with `0/O`, `1/I/l`. For example, `DOL10` could easily be read as `D0LIO`.
- **Use separators consistently and parsimoniously.** If you use hyphens, underscores, or another separator, use the same convention throughout.
- **Avoid spearators that can be easily mis-interpreted.** Avoid slashes (/), backslashes (\), spaces, commas, semicolons, colons, and other punctuation that may have special meanings in filenames, URLs, spreadsheets, or software.
- **Avoid date-like names.** Names such as `06-01` can be automatically converted to dates in spreadsheets (SGP has a sample 4011/2 which Excel converts to Feb-4011 if care is not taken)
- **Do not use depth or height as the sole identifier.** Record depth/height separately as a numerical value. It can also be incorporated into an alphanumeric sample name where useful.
- **Check existing naming systems.** If other researchers have worked at the same site, section, or region, consider whether your proposed names could duplicate theirs.

## Site Names

Use **short, simple, alphanumeric names** that are distinctive within the study and, where possible, the wider region.

Names based on local geography can be useful, but consider how distinctive the feature is. A name such as `Mill Creek` may be unsuitable if there are multiple Mill Creeks in the region, or if further sampling is likely along the same feature. A project-specific code or additional information can help.

Names or abbreviations based on the collector or project can also work well, provided they are distinctive.

## Sample Names

A sample name combining a short site identifier with a stratigraphic height or core depth can be useful—for example, `S1407-0.1`. Where a site name is longer, use a suitable abbreviation or project-specific code, such as `MCW-01`, `MCW-02`, `MCW-03`.

This approach can make samples easier to track while retaining useful information about their position. However, **always record the numerical height or depth separately**, even when it is incorporated into the sample name. Differences in formatting or precision, such as `10.05` versus `10.1`, can otherwise make matching difficult.

Most importantly, consider whether the resulting names will still be distinctive **outside your immediate project**. A small amount of additional information in a name can prevent substantial problems when datasets are combined later.
