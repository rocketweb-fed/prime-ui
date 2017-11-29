---
title: Lookbook Widgets
taxonomy:
    category: docs
---

[notice]
Currently there are 2 lookbook blocks on Homepage. You can find them in admin by looking for the following ids:
* lookbook-teaser-1  
* lookbook-anne-cole
[/notice]

To edit lookbook widgets:
1. Go to `Admin > Content > Blocks`
2. To edit already existing lookbook block, please find this block by id and open
3. Switch to HTML editor in _Content_ area
4. Edit only titles, links and images. Leave the markup and js code as is.
    ```html
    <div class="full-width">
    	<span class="fly-tips-title hidden">New Collection</span>
    	<div class="lookbook--header">
    		<h3>Lookbook Demo 1</h3>
    		<a href="{{config path='web/secure/base_url'}}lookbook-demo-1">See the Lookbook</a>
    	</div>
    	<div id="lookbook-demo-1" class="lookbook carousel">
    		<div class="item">
    			<a class="image-link" href="...">
    				<img src="{{media url=''}}" alt="Slide 1" />
    			</a>
    		</div>
    		<div class="item">
    			<a class="image-link" href="...">
    				<img src="{{media url=''}}" alt="Slide 2" />
    			</a>
    		</div>
    		<div class="item">
    			<a class="image-link" href="...">
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
    			$("#lookbook-demo-1").owlCarousel({
    				items: 3,
    				autoplay: false,
    				autoplayTimeout: 5000,
    				autoplayHoverPause: true,
    				dots: false,
    				loop: false,
    				nav: false,
    				navText: ["<em class='porto-icon-chevron-left'></em>","<em class='porto-icon-chevron-right'></em>"],
    				responsiveClass:true,
    				responsive:{
    					0:{
    						items:1,
    						nav: true
    					},
    					480:{
    						items:2,
    						nav: true
    					},
    					860:{
    						items:3,
    						nav:false
    					}
    				}
    			});
    		});
    	</script>
    ```
Pay attention to the second row on the skeleton:
`<span class="fly-tips-title hidden">New Collection</span>`
Here "New Collection" is a title for callout item on the right of the page
5.  Click "Save Block" button