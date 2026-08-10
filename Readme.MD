# Valve Reconstructions

**3D electron-microscopy reconstructions of cardiac valve tissue in a Tetralogy of Fallot model.**

🔗 **Live site:** https://theresawunderlich.github.io/ValveReconstructions/

This is the companion page for a research poster (M.J. Murdock Charitable Trust · University of Portland × OHSU). Scan the poster's QR code — or follow the link above — to watch the reconstructions behind the results.

---

## The finding

Altered blood flow in Tetralogy of Fallot (ToF) **reduced the cellular fraction of the pulmonary valve** while leaving the aortic valve unchanged — a valve-specific pattern consistent with a flow-driven effect.

| | Cellular fraction |
|---|---|
| Pulmonary valve — control | 0.51 |
| Pulmonary valve — ToF | 0.35 (~15 pp lower) |
| Aortic valve — difference | ≈ 0 |

## What's on the page

- **Reconstructions** — four rotating 3D volumes of the pulmonary valve leaflet (control vs. ToF), shown with the cellular material and nuclei highlighted, and again with just the cellular network.
- **Segmentation stills** — how the volumes are labelled: a single ground-truth slice, the 3-class volume, the nuclei in isolation, orthogonal slice views, and the aortic leaflet for comparison.

### Colour key

| Colour | Class |
|---|---|
| 🟢 Green | Cellular material |
| 🟣 Purple / magenta | Extracellular matrix |
| 🔴 Red / brown | Nuclei |
| ⬜ Grayscale | Raw tissue (in the movie renders) |

## How it was made

ToF was induced in chick embryos with cyclopamine and confirmed in vivo by ultrasound of aortic blood flow. One control and one ToF heart were prepared for **volume electron microscopy**, sampling the pulmonary and aortic valves. Tissue was split into cellular and extracellular classes with a two-class U-Net trained on hand-traced ground-truth slices; nuclei were segmented separately and carved out of the cellular class so the verified split stays fixed. Volume fractions are voxel-count ratios, independent of the voxel-size calibration.

## Repository layout

```
index.html     the page itself (single file, no build step)
videos/        four rotating 3D reconstructions (MP4)
posters/       still frames used as video thumbnails
images/        segmentation stills (PNG)
README.md      this file
```

The site is a single static page served with **GitHub Pages** — any commit to the default branch republishes it automatically.

## Authors

Theresa Wunderlich¹, Sandra Rugonyi Ph.D.², Makena Phillips², Sanjay Srikanth²
¹ University of Portland, Shiley School of Engineering · ² OHSU, Department of Biomedical Engineering

## Acknowledgements

M.J. Murdock Charitable Trust · OHSU Center for Developmental Health · OHSU School of Medicine · OHSU Office of Research & Innovation · University of Portland & Susan Murray Ph.D. · Rugonyi Lab
