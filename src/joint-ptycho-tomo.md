---
title: Joint Ptychographic Tomography
toc: false
style: css/custom.css
---

```js
const img_VLP = FileAttachment("data/joint-ptycho-tomo-VLP.svg").href;
const img_Apo = FileAttachment("data/joint-ptycho-tomo-Apo.svg").href;
const img_com = FileAttachment("data/overlap-tomo-comparison.svg").href;

import { return_resized_img } from "./components/ImageUtilities.js";
```

# Joint Ptychographic Tomography

- "Serial" ptychographic tomography: 2D projections &rarr; typical SPA workflow
  - Not maximally dose-efficient: 4D-data &rarr; 2D-projections &rarr; 3D-volume
- "Joint" ptychographic tomography: 4D-data &rarr; 3D volume
  - Captures non-linear effects of propagator (thicker samples?)
  - Allows regularization in 3D

<details open>
<summary>  Joint / Serial Ptychographic Tomography Comparison </summary>
<div class="card" style="background: white;">
  <div class="img-container">
    ${resize((width)=> return_resized_img(img_com,width,"auto;"))}
    <div style="color: var(--theme-background);"> Iterative Phase Retrieval Algorithms for Scanning Transmission Electron Microscopy, <a href="https://arxiv.org/abs/2309.05250"> arXiv:2309.05250</a> </div>
  </div>
</div>
</details>

## Simulated Joint Ptycho-Tomo Reconstructions

<div class="grid grid-cols-2" style="grid-auto-rows: auto;">
  <div class="img-container" style="min-height:300px;">
    Virus-like particles
    ${resize((width,height)=> return_resized_img(img_VLP,height-16,height-16))}
  </div>
  <div class="img-container" style="min-height:300px;">
    Apoferritin
    ${resize((width,height)=> return_resized_img(img_Apo,height-16,height-16))}
  </div>
</div>
