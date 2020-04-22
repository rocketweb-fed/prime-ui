---
title: Lazysizes
taxonomy:
    category: docs
---

| Requirejs alias | File location | File name |
| --- | --- | --- |
| lazysizes | Magento_Theme/js/ | lazysizes.js |

High performance and SEO friendly lazy loader for images (responsive and normal), iframes and more, that detects any visibility changes triggered through user interaction, CSS or JavaScript without configuration.

Script is included in footer on every page by default. Template fiel that includes configuration and requirejs script is located at [Magento_Theme/templates/html/lazysizes.phtml](https://github.com/rocketweb-fed/magento2-theme-prime/blob/master/Magento_Theme/templates/html/lazysizes.phtml)

### Usage

#### Basic usage
To trigger image lazy loading add `lazyload` class to `<img>` element and add `data-src` to point to image source
[raw]
```html
<img class="product-image-photo lazyload" 
    data-src="<?= $block->getImageUrl() ?>" 
    alt="<?=  $block->stripTags($block->getLabel(), null, true) ?>" />
```
[/raw]

#### LQIP 
When using LQIP (Low Quality Image Placeholder) approach include `src` attribute to indicate low quality image that is shown before proper image is lazyloaded. 
[raw]
```html
<img class="banner__image lazyload" 
    data-src="<?= $imageResizer->resizeAndGetUrl($imageUrl, 1200, null, []); ?>" 
    src="<?= $imageResizer->resizeAndGetUrl($imageUrl, 300, null, []); ?>"
    alt="<?=  $altText ?>" />
```
[/raw]

#### Blurred LQIP
To further enhance LQIP approach use lazysizes' blur-up feature to blur and unvail low quality image. Simply replace `src` with `data-lowsrc` to achieve the blur effect.
[raw]
```html
<img class="banner__image lazyload" 
    data-src="<?= $imageResizer->resizeAndGetUrl($imageUrl, 1200, null, []); ?>" 
    src="<?= $imageResizer->resizeAndGetUrl($imageUrl, 300, null, []); ?>"
    alt="<?=  $altText ?>" />
```
[/raw]

#### Retina support
To add support for retina devices use `data-srcset` attribute with dpr descriptors
[raw]
```html
<img 
    data-srcset="<?= $imageResizer->resizeAndGetUrl($imageMobileUrl, 800, null, []); ?> 1x, <?= $imageResizer->resizeAndGetUrl($imageMobileUrl, 800, null, []); ?> 2x"
    alt="<?= $altText; ?>"
    class="lazyload"
/>
```
[/raw]

#### Responsive images
To lazyload responsive images use `data-srcset` attributes with width descriptors
[raw]
```html
<img data-sizes="auto"
    data-srcset="<?= $imageResizer->resizeAndGetUrl($imageUrl, 480, null, []); ?> 480w, 
        <?= $imageResizer->resizeAndGetUrl($imageUrl, 800, null, []); ?> 800w,
        <?= $imageResizer->resizeAndGetUrl($imageUrl, 1100, null, []); ?> 1100w,
        <?= $imageResizer->resizeAndGetUrl($imageUrl, 1600, null, []); ?> 1600w"
    data-src="<?= $imageResizer->resizeAndGetUrl($imageUrl, 480, null, []); ?>"
    alt="<?= $altText; ?>"
    class="lazyload"
/>
```
[/raw]

>>> Adding `data-sizes="auto"` lets browser automatically calculate which image from the set to load based on the current browser width. For the auto-calulated size to work properly image width has to be calculable ie. it's width can't be set to `auto` but rather explicitly defined eg: ```img [data-sizes="auto"] { display: block; width: 100%; }```

#### Art direction
When using `<picture>` element while working with repsonsive images it is possible to set different variations of images based on device viewport using `media` queries. It can be used in conjuction with `data-srcset` attribute for adding support for retina/responsive images. 
[raw]
```html
<picture>
    <source media="--xs" data-srcset="<?= $imageResizer->resizeAndGetUrl($imageMobileUrl, 480, null, []); ?> 1x, <?= $imageResizer->resizeAndGetUrl($imageMobileUrl, 960, null, []); ?> 2x" />
    <source media="--sm" data-srcset="<?= $imageResizer->resizeAndGetUrl($imageMobileUrl, 800, null, []); ?> 1x, <?= $imageResizer->resizeAndGetUrl($imageMobileUrl, 1600, null, []); ?> 2x" />
    <source media="--md" data-srcset="<?= $imageResizer->resizeAndGetUrl($imageUrl, 1100, null, []); ?> 1x, <?= $imageResizer->resizeAndGetUrl($imageUrl, 1100, null, []); ?> 2x" />
    <source data-srcset="<?= $imageResizer->resizeAndGetUrl($imageUrl, 1600, null, []); ?> 1600w" />
    <img data-sizes="auto"
        data-src="<?= $imageResizer->resizeAndGetUrl($imageMobileUrl, 480, null, []); ?>"
        alt="<?= $altText; ?>"
        class="lazyload"
    />
</picture>
```
[/raw]

>>> Media queries in the above example are aliased via [lazysizes configuration](https://github.com/rocketweb-fed/magento2-theme-prime/blob/master/Magento_Theme/templates/html/lazysizes.phtml) to facilitate implementation

#### Lazy loading background images and assets
Lazysizes plugin allows to lazy load background images, as well as scripts, stylesheets and require.js modules.

Example background image loading:
[raw]
```html
<div class="promo lazyload" data-bg="http://local.rwprime/pub/media/wysiwyg/home/home-eco.jpg">
    <div class="banner">
        <div class="banner__content">
            <h2 class="banner__title">Promo banner</h2>
        </div>
    </div>
</div>
```
[/raw]

For further information on loading script, stylesheets and require.js modules please refer to the [official documentation](https://github.com/aFarkas/lazysizes/tree/gh-pages/plugins/unveilhooks).