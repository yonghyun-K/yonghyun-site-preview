---
layout: page
title: Gallery
permalink: /gallery/
---

<div class="gallery-grid">
  {%- for item in site.data.gallery -%}
    <div class="gallery-item">
      <img src="{{ item.src | relative_url }}" alt="{{ item.alt | escape }}">
      {%- if item.caption -%}
        <div class="gallery-caption">{{ item.caption }}</div>
      {%- endif -%}
    </div>
  {%- endfor -%}
</div>

---

### How to add images

1. Put image files into `assets/gallery/`
2. Add entries to `_data/gallery.yml` (path + caption)
