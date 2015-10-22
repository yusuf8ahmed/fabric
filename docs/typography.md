---
layout: page
title: Typography
---

Headings, paragraphs, blockquotes, and more have some global resets.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Headings

{% example html %}
<h1>h1. heading</h1>
<h2>h2. heading</h2>
<h3>h3. heading</h3>
<h4>h4. heading</h4>
<h5>h5. heading</h5>
<h6>h6. heading</h6>
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
