---
layout: page
title: Utilities
---

There are a handful of utilities in Brick for quick behaviors, floats, alignment, and more.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Floats

Quickly float something to the left or right, and clear them later.

{% example html %}
<div class="clearfix">
  <code class="left">.left</code>
  <code class="right">.right</code>
</div>
{% endexample %}

To clearfix the floats, either use the `.clearfix` class or `@include clearfix`.

## Text alignment

Change the `text-align` on elements with a class.

{% example html %}
<p class="text-left">Left aligned text.</p>
<p class="text-right">Right aligned text.</p>
<p class="text-center">Center aligned text.</p>
{% endexample %}

## Margin and padding

Easily add a standard amount of margin or padding based on the base-unit.

- `.base-margin`: Adds the base-unit (10px) amount of margin.
- `.base-margin-x2`: Adds 2x the base-unit of margin. You can use up to `.base-margin-x5`.
- `.base-margin-top`, `.base-margin-left`, `.base-margin-right`, `.base-margin-left` can all be used to only add margin in the respective direction. You can also use the multipliers, e.g. `.base-margin-top-x4`.

`.base-padding` behaves the same as above.

## Hiding/showing content based on screen size

Use the following classes if you wish for only certain content to be visible at certain screensize breakpoints:

- `.show-md`: Only show this at medium-size screens or larger. Hide for mobile.
- `.hide-md`: Only hide this at medium-size screens or larger. Show for mobile.

## Miscellaneous

- `.no-transition` disables all CSS transitions
- `.pointer` adds `cursor: pointer`
