---
layout: page
title: Guidelines
---

Best practices and guidelines for writing HTML and CSS with approachable formatting, syntax, and more.

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## HTML

### General formatting

* Use soft-tabs with a two space indent. Spaces are the only way to guarantee code renders the same in any person's environment.
* Paragraphs of text should always be placed in a `<p>` tag. Never use multiple `<br>` tags.
* Even though quotes around attributes is optional, always put quotes around attributes for readability.
* Avoid trailing slashes in self-closing elements. For example, `<br>`, `<hr>`, `<img>`, and `<input>`.
* Don't set `tabindex` manually—rely on the browser to set the order.

### Boolean attributes

Many attributes don't require a value to be set, like `disabled` or `checked`, so don't set them.

{% highlight html %}
<input type="text" disabled>

<input type="checkbox" value="1" checked>

<select>
  <option value="1" selected>1</option>
</select>
{% endhighlight %}

For more information, [read the WhatWG section](http://www.whatwg.org/specs/web-apps/current-work/multipage/common-microsyntaxes.html#boolean-attributes).

### Lean markup

Whenever possible, avoid superfluous parent elements when writing HTML. Many times this requires iteration and refactoring, but produces less HTML. For example:

{% highlight html %}
<!-- Not so great -->
<span class="avatar">
  <img src="...">
</span>

<!-- Better -->
<img class="avatar" src="...">
{% endhighlight %}

### Forms

* Lean towards radio or checkbox lists instead of select menus.
* Wrap radio and checkbox inputs and their text in `<label>`s. No need for `for` attributes here—the wrapping automatically associates the two.
* Form buttons should always include an explicit `type`. Use primary buttons for the `type="submit"` button and regular buttons for `type="button"`.

### Tables

Make use of `<thead>`, `<tfoot>`, `<tbody>`, and `<th>` tags (and `scope` attribute) when appropriate.

{% highlight html %}
<table summary="This is a chart of invoices for 2011.">
  <thead>
    <tr>
      <th scope="col">Table header 1</th>
      <th scope="col">Table header 2</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Table data 1</td>
      <td>Table data 2</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td>Table footer 1</td>
      <td>Table footer 2</td>
    </tr>
  </tfoot>
</table>
{% endhighlight %}



## SCSS

### Spacing

* Use soft-tabs with a two space indent. Spaces are the only way to guarantee code renders the same in any person's environment.
* Put spaces after `:` in property declarations.
* Put spaces before `{` in rule declarations.
* Put line breaks between rulesets.
* Place closing braces of declaration blocks on a new line.
* Each declaration should appear on its own line for more accurate error reporting.

### Formatting

* Use hex color codes `#000` unless using `rgba()` in raw CSS (SCSS' `rgba()` function is overloaded to accept hex colors as a param, e.g., `rgba(#000, .5)`).
* Avoid specifying units for zero values, e.g., `margin: 0;` instead of `margin: 0px;`.

### Misc

As a rule of thumb, avoid unnecessary nesting in SCSS. At most, aim for three levels. If you cannot help it, step back and rethink your overall strategy (either the specificity needed, or the layout of the nesting).

### Examples

Here's a good example that applies the above guidelines:

{% highlight scss %}
// Example of good basic formatting practices
.styleguide-format {
  color: #000;
  background-color: rgba(0, 0, 0, .5);
  border: 1px solid #0f0;
}
{% endhighlight %}

## Pixels vs. ems

Use `px` for `font-size`, because it offers absolute control over text. Additionally, unit-less `line-height` is preferred because it does not inherit a percentage value of its parent element, but instead is based on a multiplier of the `font-size`.

## Class naming conventions

Never reference `js-` prefixed class names from CSS files. `js-` are used exclusively from JS files.

Use the `is-` prefix for state rules that are shared between CSS and JS.

## Specificity (classes vs. ids)

Elements that occur **exactly once** inside a page should use IDs, otherwise, use classes. When in doubt, use a class name.

* **Good** candidates for ids: header, footer, modal popups.
* **Bad** candidates for ids: navigation, item listings, item view pages.

When styling a component, start with an element + class namespace (prefer class names over ids),  prefer direct descendant selectors by default, and use as little specificity as possible. Here is a good example:

{% highlight html %}
<ul class="category-list">
  <li class="item">Category 1</li>
  <li class="item">Category 2</li>
  <li class="item">Category 3</li>
</ul>
{% endhighlight %}

{% highlight scss %}
.category-list { // element + class namespace

  // Direct descendant selector > for list items
  > li {
    list-style-type: disc;
  }

  // Minimal specificity for all links
  a {
    color: #f00;
  }
}
{% endhighlight %}

### CSS Specificity guidelines

* If you must use an id selector (`#selector`) make sure that you have no more than *one* in your rule declaration. A rule like `#header .search #quicksearch { ... }` is considered harmful.
* When modifying an existing element for a specific use, try to use specific class names. Instead of `.listings-layout.bigger` use rules like `.listings-layout.listings-bigger`. Think about `ack/grep`ing your code in the future.
* The class names `disabled`, `mousedown`, `danger`, `hover`, `selected`, and `active` should *always* be namespaced by a class (`button.selected` is a good example).
