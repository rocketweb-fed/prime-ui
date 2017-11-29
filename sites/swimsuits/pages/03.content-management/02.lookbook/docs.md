---
title: Lookbook
taxonomy:
    category: docs
---

### How to create a new lookbook:
1. Go to `Admin > Content > Pages`
2. Click _Add New Page_
3. Switch to HTML editor in _Content_ area
4. Copy and paste the following markup:
```html
<div class="full-width">
	<div id="lookbook-page" class="lookbook carousel">
		<div class="item">
			<a class="image-link" href="">
				<img src="{{media url=''}}" alt="Slide 1" />
			</a>
		</div>
		<div class="item">
			<a class="image-link" href="">
				<img src="{{media url=''}}" alt="Slide 2" />
			</a>
		</div>
		<div class="item">
			<a class="image-link" href="">
				<img src="{{media url=''}}" alt="Slide 3" />
			</a>
		</div>
	</div>
</div>
<script type="text/javascript">
	require([
		'jquery',
		'owl.carousel/owl.carousel.min'
		], function ($) {
			$("#lookbook-page").owlCarousel({
				items: 3,
				autoplay: true,
				autoplayTimeout: 5000,
				autoplayHoverPause: true,
				dots: false,
				merge: true,
				loop: false,
				navRewind: false,
				nav: true,
				navText: ["<em class='porto-icon-chevron-left'></em>","<em class='porto-icon-chevron-right'></em>"],
				responsiveClass:true,
				responsive:{
					0:{
						items:1,
					},
					480:{
						items:2,
					},
					860:{
						items:3,
					}
				}
			});
		});
 </script>
```
Here, each `<div class="item">....</div>`  is  an item of carousel. You can add as many items as you need. To make the page look complete the number of these items shouldn't be less then 3.
For each item:
 - remove  `<img src="{{media url=''}}" alt="Slide 1" />`  and paste the correct image by using _Insert Image..._ button
 - add the correct 'href' attribute for `<a class="image-link" href="">` or remove the wrapper `<a class="image-link"></a>` tag and leave only `<img>` tag inside `<div class="item"></div>` if you don't have a link for this item
 ![](https://wiki.rocketweb.com/download/attachments/28279251/Lookbook_page.png)
5. You can add some own content above and below this block if you want
6. Go to Design tab and set _Layout_ to "1column"
7. Click _Save Page_ button at the top of the page

