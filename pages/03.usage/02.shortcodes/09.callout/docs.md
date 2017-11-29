---
title: Callout
taxonomy:
    category: docs
---
[raw]
The `[ui-callout]` shortcode is intended to be able to provide numbered callout badges on an image and allow you to hover over an image and see a tooltip describing a particular feature.  This is particularly useful when describing a user interface or provide notes or tips for an image.

Each `[ui-callout-item]` defines a particular item or tip that exists for the image.
```
[ui-callout]
[ui-callout-item title="Outlines" position="33%, 25%, sw"]
This administrative panel lists displays the current theme's outlines, giving you quick access 
to edit, rename, duplicate, and delete them.
[/ui-callout-item]
[ui-callout-item title="Menu Editor" position="40%, 70%, nw"]
Title field allows you to edit slider title
[/ui-callout-item]
![](slider-config.png)
[/ui-callout]
```
[/raw]

This code will output:
[ui-callout]
[ui-callout-item title="Outlines" position="33%, 25%, sw"]
This administrative panel lists displays the current theme's outlines, giving you quick access 
to edit, rename, duplicate, and delete them.
[/ui-callout-item]
[ui-callout-item title="Menu Editor" position="40%, 70%, nw"]
Title field allows you to edit slider title
[/ui-callout-item]
![](slider-config.png)
[/ui-callout]

[raw]
You can see this image has **2 items**

The `[ui-callout]` has no parameters.

The `[ui-callout-item]` shortcode that defines each item has the following parameters:

* `title` - The title of the callout
* `position` - format `Y%, X%, TIP_ORIENTATION`. The Y% and X% are measured from the top left corner.  That being `0%, 0%`, and the bottom right corner being `100%, 100%`.  The tip orientation should be one of these values: `ne, nw, se, sw`

You can use whatever markdown you wish in the item itself.  These will be represented as tooltips on hover.

You can also combine this shortcode with [Animate.css](https://daneden.github.io/animate.css/) by including the CSS class in your theme or page, and then adding top-level class entries:

```
[ui-callout class="pulse infinite animated"] 
...
[/ui-callout]
```
[/raw]