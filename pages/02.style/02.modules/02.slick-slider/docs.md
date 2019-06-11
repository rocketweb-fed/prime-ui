---
title: Slick Slider
taxonomy:
    category: docs
---


Slider component that utilizes slick.js to build responsive carousels for banners and products.
>>> This style component requires [slickSlider](/javascript/jquery/slick-slider) jquery widget in order work properly.

### Usage

[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Code"]
[raw]
```html
<div data-mage-init='{"rwSlider" : { "total": "5", "sliderConfig": { sliderConfigObj }, "breakpoints": { breakpointConfigObj } }}'>
    <div class="slide1">...</div>
    <div class="slide2">...</div>
    <div class="slide3">...</div>
</div>

```
[/raw]
[/ui-tab]
[ui-tab title="Preview"]
![Slider](slider.png)
[/ui-tab]
[/ui-tabs]


### Variables
| Variable | Default Value |
| -------- | ------------- |
| @rw-slick__icon-font | 'rw-prime' |
| @rw-slick__loader-path | '@{baseDir}images/' |
| @rw-slick__prev-character | '\62' |
| @rw-slick__next-character | '\63' |
| @rw-slick__nav-size | 25px |
| @rw-slick__dot-size | 18px |
| @rw-slick__opacity | .85 |
| @rw-slick__opacity--on-hover | 1 |
| @rw-slick__opacity--not-active | .25 |
