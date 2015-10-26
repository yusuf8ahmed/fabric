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
<p class="container-green button-example">
  <button class="button primary-action" type="button">Button button</button>
  <a class="button secondary-action" href="#" role="button">Link button</a>
</p>
{% endexample %}

You can find them in three sizes: the default `.button`, `.size-md`, and  `.size-lg`.

{% example html %}
<p class="container-green button-example">
  <button class="button" type="button">.button</button>
  <button class="button size-md" type="button">.button .size-md</button>
  <button class="button size-lg" type="button">.button .size-lg</button>
</p>
{% endexample %}

## Colors

Buttons come in several colors.

{% example html %}
<p class="container-green button-example">
  <button class="button" type="button">.button</button>
  <button class="button color-yellow" type="button">.button .color-yellow</button>
  <button class="button semitransparent" type="button">.button .color-semitransparent</button>
</p>
<p class="container-green button-example">
  <button class="button" type="button">.button</button>
  <button class="button color-yellow" type="button">.button .color-yellow</button>
  <button class="button color-semitransparent" type="button">.button .color-semitransparent</button>
</p>
{% endexample %}

## Disabled state

Unimplemented (TODO).

## Block buttons

Unimplemented (TODO). Are these needed?
