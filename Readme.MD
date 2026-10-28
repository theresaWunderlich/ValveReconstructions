# Valve Reconstructions

**3D electron-microscopy reconstructions of developing heart valve tissue in a Tetralogy of Fallot chick model, segmented with deep learning.**

🔗 **Live site:** https://theresawunderlich.github.io/ValveReconstructions/

Companion page for the research talk and poster *Quantifying Cellular Organizations in Congenital Heart Disease Models Using Electron Microscopy and Deep Learning* (M.J. Murdock Charitable Trust · University of Portland × OHSU).

---

## The finding

Altered blood flow in Tetralogy of Fallot (ToF) **reduced the cell fraction of the pulmonary valve** and increased its extracellular matrix, while the aortic valve stayed essentially unchanged: a valve-specific pattern consistent with blood flow shaping valve remodeling.

| Structure | Control | ToF |
|---|---|---|
| Pulmonary valve, cell fraction | 0.505 | 0.352 |
| Pulmonary valve, extracellular matrix | 0.495 | 0.648 |
| Pulmonary valve, nuclei | 0.080 | 0.089 |
| Aortic valve, cell fraction | 0.501 | 0.503 |
| Aorta wall, cell fraction | 0.467 | — |

40 × 40 µm interior crops, n = 1 ROI per structure per condition, raw EM (no intensity normalization).

## What's on the page

1. **Reconstructions**: tabbed ToF-vs-control viewer (pulmonary and aortic cell/matrix, 3-class with nuclei, cells + nuclei, orthogonal slices), four rotating 3D movies, and single-nucleus reconstructions from the cell-counting model.
2. **Results**: cellular density by structure; pulmonary valve compartments.
3. **Background**: CHD, the four features of ToF, hypothesis and aim.
4. **Methods**: sample collection, EM regions of interest, U-Net / U-Net++ segmentation in Dragonfly ORS.
5. **Conclusions** and **What's next**: preprocessing, cell counting, nucleoplasmic reticulum, whole image slices, more samples.

### Color key

| Color | Class |
|---|---|
| 🟢 Green | Cell material |
| 🟣 Purple / magenta | Extracellular matrix |
| 🔴 Red / brown | Nuclei |
| ⬜ Grayscale | Raw tissue |

## Editing

All captions, figures and chart numbers live in one `<script>` block at the top of `index.html` (`PAIRS`, `MOVIES`, `NUCLEI`, `CELLULAR`, `COMPARTMENTS`).

## Repository layout

```
index.html     the page (single file, no build step)
videos/        rotating 3D reconstructions (MP4)
posters/       still frames used as video thumbnails
images/        reconstruction stills, EM overviews, single-nucleus renders
Readme.MD      this file
```

Served with **GitHub Pages**; any commit to the default branch republishes it.

## Authors

Theresa Wunderlich¹, Sandra Rugonyi Ph.D.², Makena Phillips², Sanjay Srikanth²
¹ University of Portland, Shiley School of Engineering · ² OHSU, Department of Biomedical Engineering

## Acknowledgements

M.J. Murdock Charitable Trust · OHSU Center for Developmental Health · OHSU School of Medicine · OHSU Office of Research & Innovation · University of Portland & Susan Murray Ph.D. · Rugonyi Lab: Sandra Rugonyi Ph.D., Makena Phillips, Sanjay Srikanth, Marina Nimmo, Onur Mutlu
