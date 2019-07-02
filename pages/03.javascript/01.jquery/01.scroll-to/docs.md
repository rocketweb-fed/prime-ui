---
title: Scroll To
taxonomy:
    category: docs
---

Enables scrolling to anchor on the same page defined in "href" attribute of a link.

### Usage
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Code"]
[raw]
```html
<a  class="back-to-top float-button icon rw-icon-angle-up" 
    href="#top" 
    title="<?= __('Back to top') ?>" 
    data-mage-init='{"scrollTo": { "attr": "href", "offset": "130" }}'>
</a>
```
[/raw]
[/ui-tab]
[ui-tab title="Preview"]
![Sticky Header](scroll-to.png)
[/ui-tab]
[/ui-tabs]


### Options
| Option | Default Value | Purpose |
| --- | --- | --- |
| enabled | true | Enables scroll functionality |
| attr | 'href' | Attribute that defines target anchor |
| offset | 20 | Offset target elemenent is scrolled past |
| showClass | 'show' | Class responsible for toggling visibilty of the button |