# Land–Water Interface (LWI) Mapping & Land-Use Change Analysis

This repository contains code and workflows to (1) generate a EU Land–Water Interface (LWI) map from remote-sensing and geo-spatial inputs and (2) quantify land-use/land-cover (LULC) transformations within the LWI over time, with a focus on robustly classified land covers such as **cropland** and **built-up/urban** areas.

The project is designed for reproducible raster processing and analysis (tiling, masking, reclassification, gap-filling, change detection, and summary statistics).

---

## Contents
- **LWI definition**
   We defined the land-water interface as the dynamic zone in which terrestrial and aquatic systems interact most closely. On the water side, the land-water interface covers the shallow edges close to the land area, including areas that are only seasonally exposed to water, such as shoreline marshes, reed beds, and mud and sandflats. On the land side, the land-water interface is the low-lying terrestrial area that stays connected to the adjacent river, lake, or ocean water body through spatial proximity and/or because floods, back-flow, or groundwater connect these areas (e.g., floodplains, deltas, and seasonally inundated lowlands). Together, the water-side and land-side form a narrow belt, usually only 10s to 100s of meters wide, where ecological processes are linked. We applied this definition uniformly to rivers, lakes, and coastal areas.

- **LWI mapping**
   To delineate the land-water interface, we integrated 20 geospatial datasets, capturing surface-water dynamics, inundation hazard, wetlands, shorelines, or terrain morphology. We prioritized products that are open-access and have high spatial resolution (<100 m), documented accuracy, and full continental coverage, thus keeping the workflow transparent, reproducible, and transferable. In the case of dynamic features, such as surface water and floodplains, no single map accurately captures these features. We thus adopted an anchor-plus-fusion strategy: (i) we selected the best-validated, highest-resolution map as an “anchor”; and then (ii) merged one or more complementary datasets with the anchor to minimize errors of omission and resolve misclassifications. All fusions were performed after reprojecting to a common 30-m grid. For other features, such as lakes, coastlines, and digital elevation models, we adopted the single most accurate and up-to-date dataset available, thereby limiting redundancy and compound uncertainty. Our overall approach to map the land-water interface and evaluate its accuracy and completeness consisted of four main steps
  
- **Land-use change within LWI**
  - Cropland change and urbanization inside the LWI
  - Optional utilities for additional transitions (e.g., cropland–grassland) if datasets allow
- **Raster utilities**
  - NA handling / gap-filling helpers (e.g., neighborhood modal filling constrained by multi-year support)
  - Reclassification helpers and QA checks

---
