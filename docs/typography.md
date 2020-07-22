---
layout: page
title: Typography
---

Headings, paragraphs, blockquotes, and more have some global resets.

## Contents

- Will be replaced with the ToC, excluding the "Contents" header
  {:toc}

## Headers

The default `<h1>` through `<h5>` tags are bold sans-serif headers.

Optionally use CSS classes to customize the header:

- `.h1-sans` through `.h5-sans` use the sans-serif with bold font-weight.
- `.h1-sans-normal` through `.h5-sans-normal` use the sans-serif with normal font-weight.

{% example html %}

<h1>h1 Header (bold)</h1>
<h2>h2 Header (bold)</h2>
<h3>h3 Header (bold)</h3>
<h4>h4 Header (bold)</h4>
<h5>h5 Header (bold)</h5>

<h1 class="h1-sans-normal">h1 Header (normal)</h1>
<h2 class="h2-sans-normal">h2 Header (normal)</h2>
<h3 class="h3-sans-normal">h3 Header (normal)</h3>
<h4 class="h4-sans-normal">h4 Header (normal)</h4>
<h5 class="h5-sans-normal">h5 Header (normal)</h5>
{% endexample %}

## Body text

{% example html %}

<p>Nullam quis risus eget urna mollis ornare vel eu leo. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Nullam id dolor id nibh ultricies vehicula.</p>
<p>Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Donec ullamcorper nulla non metus auctor fringilla. Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit. Donec ullamcorper nulla non metus auctor fringilla.</p>
{% endexample %}

## Lead

Make a paragraph stand out by adding `.p1` or `.p2`.

{% example html %}

<p class="p1">
  Nullam quis risus eget urna mollis ornare vel eu leo.
</p>

<p class="p2">
  Vivamus sagittis lacus vel augue laoreet rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus.
</p>
{% endexample %}

## Inline text elements

Styling for common inline HTML5 elements.

{% example html %}

<p><u>This line of text will render as underlined</u></p>
<p><small>This line of text is meant to be treated as fine print.</small></p>
<p><strong>This line rendered as bold text.</strong></p>
<p><em>This line rendered as italicized text.</em></p>
{% endexample %}

## Blockquotes

Wrap `<blockquote>` around any HTML as the quote.

{% example html %}

<blockquote>
  “Lorem ipsum dolor sit amet, consectetur adipiscing elit. Integer posuere erat a ante.”
</blockquote>
{% endexample %}

## Uppercase

There are uppercase mixins and classes that can be included in different rules.

{% example html %}

<div class="uppercase-sans-bold">
  .uppercase-sans-bold
</div>
<div class="uppercase-text">
  .uppercase-text
</div>
{% endexample %}

## Content

Text may be styled using the `.content` class. There are four available font-sizes for `.content`: `.size-xs`, `.size-sm`, `.size-md` and `.size-lg`. This is particularly useful when styling text within [cards](../layout/#cards).

{% example html %}

<div class="row-md">
  <div class="col-3">
    <div class="content size-xs">
      .content .size-xs
    </div>
  </div>
  <div class="col-3">
    <div class="content size-sm">
      .content .size-sm
    </div>
  </div>
  <div class="col-3">
    <div class="content size-md">
      .content .size-md
    </div>
  </div>
   <div class="col-3">
     <div class="content size-lg">
       .content .size-lg
     </div>
  </div>
</div>
{% endexample %}

## Numbers

Numbers may have a `.number-title` label, `.number-value` is used to denote values. Similar to `.content`, there are four different sizes available for numbers: `.size-xs`, `.size-sm`, `.size-md` and `.size-lg`.

{% example html %}

<div class="number-title">
  .number-title
</div>
<div class="number-value size-md">
  0.00
</div>
{% endexample %}

## Colors

There are mixins provided to easily color text. Simply add `@include text-green` (and so on) to your rule.

{% example html %}

<div class="text-green">
  You can have green text,
</div>
<div class="text-green-dark">
  dark green text,
</div>
<div class="text-red">
  red text,
</div>
<div class="text-yellow">
  yellow text,
</div>
<span class="text-white brand-primary-bg">
  white text,
</span>
<div class="text-gray">
  gray text,
</div>
<div class="text-gray-hover">
  or gray text on hover.
</div>
{% endexample %}

## Social icons

## Icons

{% example html %}

<div class="ws-icon-info">
</div>
{% endexample %}
