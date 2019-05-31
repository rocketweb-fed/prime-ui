---
title: Icons
taxonomy:
    category: docs
---

[FontAwesome](https://fortawesome.github.io/Font-Awesome/) is a powerful library of font-based icons. This shortcode makes it simple to add fontawesome icons to your page content without using HTML.

Simplest Format
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Shortcode"]
[raw]
```
[fa=cog /] 
```
[/raw]
[/ui-tab]
[ui-tab title="Output"]
[fa=cog /] 
[/ui-tab]
[/ui-tabs]


Format using `fa-` prefix
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Shortcode"]
[raw]
```
[fa=fa-cog /] 
```
[/raw]
[/ui-tab]
[ui-tab title="Output"]
[fa=fa-cog /] 
[/ui-tab]
[/ui-tabs]


Explicit format
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Shortcode"]
[raw]
```
[fa icon=fa-camera-retro /]
```
[/raw]
[/ui-tab]
[ui-tab title="Output"]
[fa icon=fa-camera-retro /]
[/ui-tab]
[/ui-tabs]


Explicit format with extras - [See FontAwesome Examples](https://fortawesome.github.io/Font-Awesome/examples/)
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Shortcode"]
[raw]
```
[fa icon=fa-camera-retro extras=fa-4x /] 
```
[/raw]
[/ui-tab]
[ui-tab title="Output"]
[fa icon=fa-camera-retro extras=fa-4x /] 
[/ui-tab]
[/ui-tabs]


The full monty! - [See FontAwesome Examples](https://fortawesome.github.io/Font-Awesome/examples/)
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Shortcode"]
[raw]
```
[fa icon=fa-circle-o-notch extras=fa-spin,fa-3x,fa-fw,margin-bottom /] 
```
[/raw]
[/ui-tab]
[ui-tab title="Output"]
[fa icon=fa-circle-o-notch extras=fa-spin,fa-3x,fa-fw,margin-bottom /] 
[/ui-tab]
[/ui-tabs]