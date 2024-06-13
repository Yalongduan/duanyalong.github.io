---
title: Portfolio
layout: collection
category: foo
permalink: /portfolio/
collection: portfolio
entries_layout: grid
classes: wide
excerpt: "节选，内容简要"
gallery:
  - url: /assets/images/road.jpg
    image_path: /assets/images/road.jpg
    alt: "placeholder image 1"
    title: "Image 1 title caption"
  - url: /assets/images/road.jpg
    image_path: /assets/images/road.jpg
    alt: "placeholder image 2"
    title: "Image 2 title caption"
  - url: /assets/images/road.jpg
    image_path: /assets/images/road.jpg
    alt: "placeholder image 3"
    title: "Image 3 title caption"
---
{% include figure popup=true image_path="/assets/images/road.jpg" alt="this is a placeholder image" caption="This is a figure caption." %}
<figure>
  <a href="/assets/images/road.jpg" class="image-popup" title="This is a figure caption.">
    <img src="/assets/images/road.jpg" alt="this is a placeholder image">
  </a>
  <figcaption>This is a figure caption.</figcaption>
</figure>

{% include gallery caption="This is a sample gallery with **Markdown support**." %}
**测试“”** 测试
# 一级标题
## 二级标题
### 三级标题

{% capture written_label %}'None'{% endcapture %}

{% for collection in site.collections %}
  {% unless collection.output == false or collection.label == "posts" %}
    {% capture label %}{{ collection.label }}{% endcapture %}
    {% if label != written_label %}
      <h2 id="{{ label | slugify }}" class="archive__subtitle">{{ label }}</h2>
      {% capture written_label %}{{ label }}{% endcapture %}
    {% endif %}
  {% endunless %}
  {% for post in collection.docs %}
    {% unless collection.output == false or collection.label == "posts" %}
      {% include archive-single.html %}
    {% endunless %}
  {% endfor %}
{% endfor %}