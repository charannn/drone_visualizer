# Real Estate Drone Visualizer — MVP (Orthomosaic + AI)

This repository contains a minimal prototype backend for processing orthomosaic images (stitched top-down drone maps) to:

- Detect parcel/field boundaries using simple CV
- Vectorize detected boundaries to polygons
- Compute area (supports GeoTIFF / manual pixel->meter scale)
- Expose endpoints via FastAPI for integration with Flutter UI

> Note: Orthomosaic images alone cannot be used to create 3D models. For 3D reconstruction you need the original overlapping drone photos.

## Quickstart

1. Clone repository
2. Create virtualenv and install requirements:
```bash
python -m venv venv
source venv/bin/activate       # or venv\\Scripts\\activate on Windows
pip install -r requirements.txt
