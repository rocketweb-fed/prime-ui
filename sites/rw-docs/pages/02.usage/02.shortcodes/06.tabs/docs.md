---
title: Tabs
taxonomy:
    category: docs
---

An example of the Tabs shortcode is as follows:

[raw]
```
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="First Tab"]

In tempor sed sapien eu porttitor. Aliquam cursus facilisis ante. Etiam neque nunc, blandit vel lacus et, faucibus accumsan lacus. Proin posuere varius purus quis faucibus. Quisque et enim vitae orci [placerat tincidunt](#) id ac eros. Fusce et gravida libero. 

Phasellus cursus odio ex, in **mattis lorem tincidunt** vel. Donec nibh odio, dapibus non ligula a, semper ornare massa. Nulla consectetur eu nunc sed ultrices. Integer at turpis dolor.

[/ui-tab]
[ui-tab title="Second Tab"]

In tempor sed sapien **eu porttitor**. Aliquam cursus facilisis ante. Etiam neque nunc, blandit vel lacus et, faucibus accumsan lacus. Proin posuere varius purus quis faucibus. [Quisque et enim](#) vitae orci placerat tincidunt id ac eros. Fusce et gravida libero. 

Phasellus cursus odio ex, in mattis lorem tincidunt vel. [Donec nibh odio](#), dapibus non ligula a, semper ornare massa. Nulla consectetur eu nunc sed ultrices. Integer at turpis dolor.

[/ui-tab]
[/ui-tabs]
```
[/raw]

This code will output:
[ui-tabs position="top-left" active="0"]
[ui-tab title="First Tab"]

In tempor sed sapien eu porttitor. Aliquam cursus facilisis ante. Etiam neque nunc, blandit vel lacus et, faucibus accumsan lacus. Proin posuere varius purus quis faucibus. Quisque et enim vitae orci [placerat tincidunt](#) id ac eros. Fusce et gravida libero. 

Phasellus cursus odio ex, in **mattis lorem tincidunt** vel. Donec nibh odio, dapibus non ligula a, semper ornare massa. Nulla consectetur eu nunc sed ultrices. Integer at turpis dolor.

[/ui-tab]
[ui-tab title="Second Tab"]

In tempor sed sapien **eu porttitor**. Aliquam cursus facilisis ante. Etiam neque nunc, blandit vel lacus et, faucibus accumsan lacus. Proin posuere varius purus quis faucibus. [Quisque et enim](#) vitae orci placerat tincidunt id ac eros. Fusce et gravida libero. 

Phasellus cursus odio ex, in mattis lorem tincidunt vel. [Donec nibh odio](#), dapibus non ligula a, semper ornare massa. Nulla consectetur eu nunc sed ultrices. Integer at turpis dolor.

[/ui-tab]
[/ui-tabs]

[raw]
The `[ui-tabs]` shortcode has some optional parameters:

* `position` - top-left | top-right | bottom-left | bottom-right
* `active` - 0-index number of initial active tab state.  0 to (number of tabs - 1)
* `theme` - default | lite | badges

The `[ui-tab]` shortcode that defines each _tab_ has the following parameters:

* `title` - The text to display for the actual tab title
[/raw]

You can use whatever markdown you wish in the tab itself.  They are auto-adjusting and fully responsive.