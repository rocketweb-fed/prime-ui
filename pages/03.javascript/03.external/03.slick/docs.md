---
title: Slick
taxonomy:
    category: docs
---

| Requirejs alias | File location | File name |
| --- | --- | --- |
| slick | WeltPixel_OwlCarouselSlider/js/ | slick.min.js |

The last carousel you'll ever need. Responsive, scalable, includes lazy loading.

Slick is used as dependancy in rwSlider component and powers all carousels in Prime.

### Usage
To trigger image lazy loading add `lazyload` class to `<img>` element via template.
[raw]
```js
slider.slick({
    autoplay: true,
    autoplaySpeed: 3000,
    adaptiveHeight: true,
    arrows: true,
    dots: false,
    lazyLoad: "ondemand",
    infinite: false,
    centerPadding: 0,
    slidesToShow: 5,
    slidesToScroll: 1,
    fade: false,
    responsive: [
    {
      breakpoint: 1024,
      settings: {
        slidesToShow: 3,
        slidesToScroll: 3,
        infinite: true,
        dots: true
      }
    },
    {
      breakpoint: 600,
      settings: {
        slidesToShow: 2,
        slidesToScroll: 2
      }
    },
    {
      breakpoint: 480,
      settings: {
        slidesToShow: 1,
        slidesToScroll: 1
      }
    }]
}
```
[/raw]

