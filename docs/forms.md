---
layout: page
title: Forms
---

Style individual form controls and utilize common layouts.

<div class="flash">
  <strong>Heads up!</strong> Forms need some reworking to clean up the specificity and required markup. We'll get to that soon!
</div>

## Contents

* Will be replaced with the ToC, excluding the "Contents" header
{:toc}

## Example form

Form elements in Fabric currently have no basic layout specified (this is by design). You'll need to use `<fieldset>`s, `<div>`s, or other elements and styles to rearrange them.

{% example html %}
<form>
  <input type="text" class="form-input-text" placeholder="Name">
  <input type="email" class="form-input-text" placeholder="Email address">

  <p>
    <label>
      <input type="checkbox"> Remember me
    </label>
  </p>

  <p>
    <label>
      <input type="radio" id="herp" name="herpderp" checked> Herp
    </label>
    <label>
      <input type="radio" id="derp" name="herpderp"> Derp
    </label>
  </p>

  <p>
    <button class="button button-yellow" type="submit">Submit</button>
  </p>
</form>
{% endexample %}

## Colors

The default text inputs has a white background, but you can append the `.color-beige` class to make it beige.

{% example html %}
<form>
  <input class="form-input-text" type="text" placeholder=".form-input-text (default)">
  <input class="form-input-text color-beige" type="text" placeholder=".form-input-text .color-beige">
</form>
{% endexample %}

## Sizes

There are two input sizes: medium and small. (TODO: consider adding more sizes as necessary).

Medium is the default size, but you can apply the `.size-sm` class to make it small.

{% example html %}
<form>
  <input class="form-input-text" type="text" placeholder="medium (default)">
  <input class="form-input-text size-sm" type="text" placeholder=".size-sm">
</form>
{% endexample %}

## Selects

TODO

## Checkboxes and radios

TODO - use iCheck plugin

## Form groups

TODO

## Form validation

TODO
