# BIM-FM Platform – UAV-based inspection + deep learning + BIM asset management

This repository accompanies the manuscript:

**"From UAV Inspection to Asset Management: Integration of Deep Learning for Exposed Reinforcement Detection"**  

The repository contains demonstration videos of the BIM-FM platform, a web-based system developed to integrate automated UAV inspection (exposed rebar detection using Swin Transformer + DeepLabV3) with BIM‑enabled asset management.

## Platform overview (methodology – Section 3.4)

The BIM-FM platform provides a complete workflow for infrastructure asset management:

- **Asset registration** – add/update assets, upload IFC models, set geolocation.
- **IFC 3D viewer** – interactive visualization (Three.js / web-ifc-three).
- **Inspection management** – register inspections, upload images/videos, trigger AI analysis.
- **AI module** – segmentation with SwinTransformer + DeepLabV3 (threshold = 0.50, min. pixels = 50).
- **Expert validation** – human‑in‑the‑loop review (confirm/reject/correct detections).
- **Severity Map** – color‑coded IFC elements (red = critical, green = good).
- **Dashboard & maintenance calendar** – georeferenced map, condition indicators, planning.

📺 **Video 1 – Platform overview (BIM-FM platform demonstration)**  
*Corresponds to Section 3.4 (Methodology).*  
Link to video 1: https://drive.google.com/file/d/1UiZxcB-lhE04fDdXeG5Y34GZAnrh1ghp/view?usp=drive_link
## End‑to‑end inspection workflow (results – Section 4.3)

The second video demonstrates a complete inspection cycle using the Arquiteto Paulo Casé Bridge case study:

- Upload of UAV inspection video → automatic frame extraction.
- AI processing (≈ 3 min for 99 frames, ~0.04 s per image).
- Results page: summary, frame‑by‑frame heatmaps, binary masks.
- Frame validation: inspector accepts/rejects detections, can manually mark false negatives.
- Immediate update of the IFC model (Severity Map) and dashboard.

📺 **Video 2 – End‑to‑end inspection (AI analysis + validation + BIM update)**  
*Corresponds to Section 4.3 (Results and Discussion).*  
Link to video 2: https://drive.google.com/file/d/1ATy6INKe1oEavJcPKUSkSyYDofvxmqcc/view?usp=drive_link

## Requirements & reproducibility

- Backend: Python 3.10+, FastAPI, PostgreSQL, PyTorch, IfcOpenShell.
- Frontend: React 18, TypeScript, Three.js, web-ifc-three, Leaflet.
- Hardware (testing): 13th Gen i5‑13420H, 16 GB RAM, RTX 4050.

The platform is fully replicable; source code can be shared upon request (or link to private repo if applicable).  
For dataset access or any inquiries, please contact the authors.

---
