# Land–Water Interface (LWI) Mapping & Land-Use Change Analysis

This repository contains code and workflows to (1) generate a EU Land–Water Interface (LWI) map from remote-sensing and geo-spatial inputs and (2) quantify land-use/land-cover (LULC) transformations within the LWI over time, with a focus on robustly classified land covers such as **cropland** and **built-up/urban** areas.

The project is designed for reproducible raster processing and analysis (tiling, masking, reclassification, gap-filling, change detection, and summary statistics).

---

## Contents

- **LWI mapping**
  - Build LWI masks/zones using thresholds and spatial rules
  - Produce LWI products
- **Land-use change within LWI**
  - Cropland change and urbanization inside the LWI
  - Optional utilities for additional transitions (e.g., cropland–grassland) if datasets allow
- **Raster utilities**
  - NA handling / gap-filling helpers (e.g., neighborhood modal filling constrained by multi-year support)
  - Reclassification helpers and QA checks

---
