---
toc: false
style: css/index.css
---

```js
const img_VLP = FileAttachment("data/joint-ptycho-tomo-VLP.svg").href;
const img_Apo = FileAttachment("data/joint-ptycho-tomo-Apo.svg").href;

const img_style = "object-fit:contain;";
import { return_resized_img } from "./components/ImageUtilities.js";
```

:::hero

# Joint Ptychographic Tomography for Cryo EM

:::

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

::: hero

Georgios Varnavides | National Center for Electron Microscopy  
Follow along! https://gvarnavides.com/2024emc-cryo/

:::
