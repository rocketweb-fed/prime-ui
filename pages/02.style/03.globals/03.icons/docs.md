---
title: Icons
taxonomy:
    category:
        - docs
---

Icons are implemented via icon font and can be displayed by adding class that includes icon name. 

### Usage 

[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Code"]
[raw]
```html
<span class="icon medium rw-icon-social-pt"></span>
<span class="icon medium rw-icon-social-fb"></span>
<span class="icon medium rw-icon-social-tw"></span>
<span class="icon medium rw-icon-social-ig"></span>
<span class="icon medium rw-icon-cart"></span>
<span class="icon medium rw-icon-zoom"></span>
<span class="icon medium rw-icon-quotes"></span>
<span class="icon medium rw-icon-tooltip"></span>
<span class="icon medium rw-icon-trash"></span>
<span class="icon medium rw-icon-person"></span>
<span class="icon medium rw-icon-close"></span>
<span class="icon medium rw-icon-tick"></span>
<span class="icon medium rw-icon-eyebrow"></span>
<span class="icon medium rw-icon-angle-down"></span>
<span class="icon medium rw-icon-angle-left"></span>
<span class="icon medium rw-icon-angle-right"></span>
<span class="icon medium rw-icon-angle-up"></span>
<span class="icon medium rw-icon-calendar"></span>
<span class="icon medium rw-icon-folder"></span>
<span class="icon medium rw-icon-tag"></span>
<span class="icon medium rw-icon-comment"></span>
```
[/raw]
[/ui-tab]
[ui-tab title="Preview"]
![Icons](icons.png)
[/ui-tab]
[/ui-tabs]

### Classes
| Class | Purpose |
| --- | --- |
| icon / rw-icon | Specifies default icon size (@rw-icon__size) |
| large / medium / small | Specifies icon sizes  |
| rw-icon-{icon-name} | Assigns font character to an element via content property for displaying proper icon |



### Variables
| Variable | Default Value |
| -------- | ------------- |
| @rw-icon__font | 'rw-prime' |
| @rw-icon__size | 24px |
| @rw-icon__size--l | 40px |
| @rw-icon__size--m | 32px |
| @rw-icon__size--s | 18px |

