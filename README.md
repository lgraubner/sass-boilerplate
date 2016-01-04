# Base SASS project

Starting point for new projects.

## Helpers

You can either use an helper by adding it's class or include it by using the SASS placeholder.

### clearfix

Adds a clearfix to the element.

```SASS
.clearfix {
    &:before, &:after {
        content: "";
        display: table;
    }
    &:after {
        clear: both;
    }
}
```

```HTML
// usage as class
<div class="clearfix">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %clearfix;
}
```

### hidden

Hides an element.

```CSS
.hidden {
    display: none !important;
}
```

```HTML
// usage as class
<div class="hidden">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %hidden;
}
```

### visible

Shows an element.

```CSS
.visible {
    display: block !important;
}
```

```HTML
// usage as class
<div class="visible">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %visible;
}
```

### invisible

Hides an element without taking it out of the document flow.

```CSS
.invisible {
    border: 0;
    clip:rect(0 0 0 0);
    height: 1px;
    margin: -1px;
    overflow: hidden;
    padding: 0;
    position: absolute;
    width: 1px;
}
```

```HTML
// usage as class
<div class="invisible">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %invisible;
}
```

### float-left

Floats an element to the left.

```CSS
.float-left {
    float: left;
}
```

```HTML
// usage as class
<div class="float-left">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %float-left;
}
```

### float-right

Floats an element to the right.

```CSS
.float-right {
    float: right;
}
```

```HTML
// usage as class
<div class="float-right">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %float-left;
}
```

### img-responsive

Makes an image behave responsive.

```CSS
.img-responsive {
    height: auto;
    max-width: 100%;
    display: block;
}
```

```HTML
// usage as class
<img src="..." class="img-responsive">
```

```SASS
// usage as placeholder
.element {
    @extend %img-responsive;
}
```

### text-left

Aligns text to the left.

```CSS
.text-left {
    text-align: left;
}
```

```HTML
// usage as class
<div class="text-left">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %text-left;
}
```

### text-right

Aligns text to the right.

```CSS
.text-right {
    text-align: right;
}
```

```HTML
// usage as class
<div class="text-right">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %text-right;
}
```

### text-center

Aligns text to the center.

```CSS
.text-center {
    text-align: center;
}
```

```HTML
// usage as class
<div class="text-center">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %text-center;
}
```

### text-justify

Justifies text.

```CSS
.text-justify {
    text-align: justify;
}
```

```HTML
// usage as class
<div class="text-justify">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %text-justify;
}
```

### text-uppercase

Transforms text to uppercase.

```CSS
.text-uppercase {
    text-transform: uppercase;
}
```

```HTML
// usage as class
<div class="text-uppercase">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %text-uppercase;
}
```

### text-hide

Hides text for the visitor. Useful for elements with background images as alternate text.

```CSS
.text-hide {
    text-indent: -9999px;
    overflow: hidden;
    display: block;
}
```

```HTML
// usage as class
<div class="text-hide">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %text-hide;
}
```

### block-center

Centers an element.

```CSS
.block-center {
    display: block;
    margin-left: auto;
    margin-right: auto;
}
```

```HTML
// usage as class
<div class="block-center">...</div>
```

```SASS
// usage as placeholder
.element {
    @extend %block-center;
}
```


## SASS mixins

### prefix

Prefixes css properties with vendor prefixes.

**Usage**:

```SASS
.element {
    @include prefix((
        border-radius: 5px,
        appearance: button
    ), webkit moz);
}
```

**Output**:

```CSS
.element {
    -webkit-border-radius: 5px;
    -moz-border-radius: 5px;
    border-radius: 5px;
    -webkit-appearance: button;
    -moz-appearance: button;
    appearance: button;
}
```

You can omit the vendor prefixes. By default `-webkit`, `-moz`, `-ms` and `-o` will be added to each property.

### font-size

Converts `font-size` values to rem and adds a callback. The calculated font size is based on an estimated base font size of 16px.

**Usage**:

```SASS
.element {
    @include font-size(20px);
}
```

**Output**:

```CSS
.element {
    font-size: 20px;
    font-size: 1.25rem;
}
