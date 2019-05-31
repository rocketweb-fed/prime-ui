---
title: Lazysizes
taxonomy:
    category: docs
---

| Requirejs alias | File location | File name |
| --- | --- | --- |
| lazysizes | Magento_Theme/js/ | lazysizes.js |

High performance and SEO friendly lazy loader for images (responsive and normal), iframes and more, that detects any visibility changes triggered through user interaction, CSS or JavaScript without configuration.

Script is included in footer on every page by default.

## Usage

To trigger image lazy loading add `lazyload` class to `<img>` element via template.
[raw]
```html
<img class="product-image-photo lazyload" 
    data-src="<?= $block->getImageUrl() ?>" 
    alt="<?=  $block->stripTags($block->getLabel(), null, true) ?>" />
```
[/raw]

