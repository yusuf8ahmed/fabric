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

Form elements in Brick currently have no basic layout specified (this is by design). You'll need to use `<fieldset>`s, `<div>`s, or other elements and styles to rearrange them.

{% example html %}
<form>
  <input type="text" class="form-element form-element-white" placeholder="Name">
  <input type="email" class="form-element form-element-white" placeholder="Email address">

  <label>
    <input type="checkbox"> Remember me
  </label>

  <label>
    <input type="radio" id="herp" name="herpderp" checked> Herp
  </label>
  <label>
    <input type="radio" id="derp" name="herpderp"> Derp
  </label>

  <button class="button button-yellow" type="submit">Submit</button>
</form>
{% endexample %}

## Colors

Text inputs can have a white or beige background, depending on the class you use.

{% example html %}
<form>
  <input class="form-element form-element-white" type="text" placeholder=".form-element-white">
  <input class="form-element form-element-beige" type="text" placeholder=".form-element-beige">
</form>
{% endexample %}

TODO - why are these different sizes?

## Sizes

TODO - multiple sizes: small, medium, large

## Selects

TODO

## Checkboxes and radios

TODO - use iCheck plugin

## Form groups

TODO

## Form validation

TODO
