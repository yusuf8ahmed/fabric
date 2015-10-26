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
<button class="button primary-action" type="button">Button button</button>
<a class="button primary-action" href="#" role="button">Link button</a>
{% endexample %}

You can find them in three sizes: the default `.button`, `.size-md`, and  `.size-lg`.

{% example html %}
<button class="button primary-action" type="button">.button</button>
<button class="button primary-action size-md" type="button">.button .size-md</button>
<button class="button primary-action size-lg" type="button">.button .size-lg</button>
{% endexample %}

## Colors

Buttons come in two colors. `.primary-action` is yellow, and `.secondary-action` is white.

- `.primary-action` should be used for actions such form submission and "Next".
- `.secondary-action` should be used to actions such as "Cancel" and "Back".

{% example html %}
<button class="button primary-action" type="button">.button.primary-action</button>
<button class="button secondary-action" type="button">.button.secondary-action</button>
{% endexample %}

In rare cases where the container's background color is not white, you can manually override the color in SCSS by using `@include white-button` for the primary action.

## Disabled state

Unimplemented (TODO).

## Block buttons

Unimplemented (TODO). Are these needed?
