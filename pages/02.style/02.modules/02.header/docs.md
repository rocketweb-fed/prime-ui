---
title: Header
taxonomy:
    category: docs
---


Header UI element consists of a couple of wrapper containers defined in layout files as well as classes. Typical structure of header can be found below. To modify, remove or move containers use layout directives in default.xml

### Usage

[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Code"]
[raw]
```html
<header class="page-header">
    <div class="header content">
        <div class="logo-container">...</div>
        <div class="search-container">...</div>
        <div class="links-container">...</div>
    </div>
</header>
```
[/raw]
[/ui-tab]
[ui-tab title="Preview"]
![Slider](header.png)
[/ui-tab]
[/ui-tabs]


### Layout
| Container name | Alias | Classes assigned |
| --- | --- |
| header-wrapper | | header content flex flex--wrap |
| header.logo | logo-container | flex__item flex logo-container |
| header.search | search-container | flex__item flex search-container hidden-m |
| header.links | links-container | flex__item flex links-container |


### Classes
| Class | Purpose |
| --- | --- |
| header | Sets flex layout on header parent container |
| preheader | Defines text properties for eyebrow element |
| sticky-header | Defines styles for fixed header on desktop and mobile |
| header-dropdown | Applies dropdown mixin on header action items |
| logo-container / search-container / links-container / toggle-wrapper | Apply layout styles to main header sections |