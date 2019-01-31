scss flex-grid system
====================================

## Description

Includes
* Flex
* Grid
* Mixins
* Default modifiers

## How to use
### Grid

```html
<div class="container">
  <div class="grid-row">
    <div class="grid-md-6"></div>
    <div class="grid-md-6"></div>
  </div>
</div>
```
### Flex

```html
<div class="container">
  <div class="flex">
    <div class="flex-md-6"></div>
    <div class="flex-md-6"></div>
  </div>
</div>
```

#### Flex alignment classes:
Alligns all content in flex container to:
* `flex-top` - top
* `flex-middle` - vertically middle
* `flex-bottom` - bottom
* `flex-center` - horizontally middle
* `flex-right` - right
* `flex-vh-middle` - vertically and horizontally middle

### Modifiers
#### Grid / Flex modifiers
##### Spacing
* `grid-row--include-margin` and `flex--include-margin` - Includes margin bottom to grid children
* `grid-row--no-gutter` and `flex--no-gutter` - Removes all padding from grid children
* `grid-row--small-padding` and `flex--small-padding` - Adds smaller padding to grid children
* `grid-row--extra-small-padding` and `flex--extra-small-padding` - Similar to previous modifier with reduced padding

##### Offsets
* `grid-{media-size}-offset-{index}` and `flex-{media-size}-offset-{index}` - Adds column margin left at defined media size according to grid index
* `grid-{media-size}-no-offset` and `flex-{media-size}-no-offset` - Removes column margin left at defined media size

##### Positioning
* `grid-{media-size}-push-{index}` and `flex-{media-size}-push-{index}` - Moves column position left at defined media size according to grid index
* `grid-{media-size}-pull-{index}` and `flex-{media-size}-pull-{index}` - Moves column position right at defined media size according to grid index

##### Positioning (Flex only)
* `flex-{media-size}-order-first` - Orders specific grid column at defined media size to the front
* `flex-{media-size}-order-last` - Orders specific grid column at defined media size to the end
* `flex-{media-size}-order-{index}` - Orders specific grid column at defined media size

#### General modifiers
* `hidden` - Hides element at all media sizes
* `hidden-{media-size}` - Hides element at defined media size
* `no-padding` - Removes all padding from element
* `no-padding-{media-size}` - Removes all padding from element at defined media size
* `relative` - Makes element position relative
* `block` - Makes element display as block

Alligns all content in container to:
* `align-top` - top (vertical align - works for inline/inline-block or table cell elements)
* `align-middle` - vertically middle (vertical align - works for inline/inline-block or table cell elements)
* `align-bottom` - bottom (vertical align - works for inline/inline-block or table cell elements)
* `align-left` - left
* `align-center` - horizontally middle
* `align-right` - right

Float clearing
* `clear` - Fixes float element sizes inside elements

## Flex / Grid padding overwriting
_grid.scss includes following default variables:
Create same variable in _variables.scss with your own value to overwrite the default ones.

```scss
$xs: 0px !default;
$sm: 576px !default;
$md: 768px !default;
$lg: 992px !default;
$xl: 1280px !default;

$media-sizes: (
    ("xs", $xs, false, true),
    ("sm", $sm, true, true),
    ("md", $md, true, true),
    ("lg", $lg, true, true),
    ("xl", $xl, true, false)
) !default;

$grid-length: 12 !default;

$grid-padding: 15px !default;
$grid-padding-small: 10px !default;
$grid-padding-extra-small: 5px !default;

$grid-spacing-bottom: 30px !default;
```
