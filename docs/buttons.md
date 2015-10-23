---
layout: page
title: Buttons
---

Buttons are used for **actions**, like in forms, while textual hyperlinks are used for **destinations**, or moving from one page to another.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Default buttons

Use the `.button` for form actions and primary page actions. These are used extensively around the site.

When using a `<button>` element, **always specify a `type`**. When using a `<a>` element, **always add `role="button"` for accessibility**.

{% example html %}
<p class="button-example">
  <button class="button" type="button">Button button</button>
  <a class="button" href="#" role="button">Link button</a>
</p>
{% endexample %}

You can find them in three sizes: the default `.button`, `.buttom-medium`, and  `.buttom-large`.

{% example html %}
<p class="button-example">
  <button class="button" type="button">Button</button>
  <button class="button button-medium" type="button">Medium button</button>
  <button class="button button-large" type="button">Large button</button>
</p>
{% endexample %}

## Colors

Buttons come in several colors. The default is a white background with black text.

{% example html %}
<p class="button-example">
  <button class="button" type="button">Default button</button>
  <button class="button button-yellow" type="button">Yellow button</button>
  <button class="button button-semitransparent" type="button">Semitransparent button</button>
</p>
{% endexample %}

## Disabled state

Unimplemented (TODO).
