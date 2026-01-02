---
layout: page
permalink: /publications/
title: Publications
description:
topics:
  - name: Graph Learning
    description: Research on graph neural networks, graph representation learning, and network analysis
  - name: Signal Processing
    description: Techniques for analyzing and modeling signals across time, space, and/or frequency domains
  - name: Other Applications
    description: Miscellaneous research applications
nav: true
nav_order: 1
---

<!-- _pages/publications.md -->

<div class="publications">

{%- for topic in page.topics %}

<h2 class="topic">{{ topic.name }}</h2>
<p class="topic-description" style="color: var(--global-text-color-light); margin-bottom: 1rem; font-style: italic;">{{ topic.description }}</p>
  {% bibliography -f {{ site.scholar.bibliography }} -q @*[topic={{ topic.name }}]* %}
{% endfor %}

</div>
