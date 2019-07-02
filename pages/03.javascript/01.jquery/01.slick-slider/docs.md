---
title: Slick Slider
taxonomy:
    category: docs
---

Widget enables slider functionality for displaying banner and product carousels.

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


### Options
| Option | Default Value | Purpose |
| --- | --- | --- |
| total | 0 | Defines number of slides |
| type | 'widget-product-slider' | Defines slider type |
| sliderConfig | {} | Slider configuration object. See [this page](https://kenwheeler.github.io/slick/) for reference |
| breakpoint | {} | Breakpoint configuration object |