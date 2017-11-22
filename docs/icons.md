---
layout: page
title: Icons
---

Fabric includes icons.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Coloring

Icons can be colored by passing a hex value to the icon mixin. The base classes are in gray.

Example SCSS class: `.info-red-example { @include ws-icon-info($color-red); }`

{% example html %}
<svg class="info-red-example"></svg>
{% endexample %}

## arrow-down

{% example html %}
<svg class="ws-icon-arrow-down"></svg>
{% endexample %}

## info

{% example html %}
<svg class="ws-icon-info"></svg>
{% endexample %}

## three-dot-spinner

{% example html %}
<svg class="ws-icon-three-dot-spinner"></svg>
{% endexample %}
