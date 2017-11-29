---
title: Category Listing
taxonomy:
    category: docs
---

[ui-browser address="http://yourstore.com"]
![](https://wiki.rocketweb.com/download/attachments/23955077/HP-categlist.jpg)
[/ui-browser]

In order to edit the category listing on homepage got to `Admin > Content > Block` and select *Homepage Categories list*
![](https://wiki.rocketweb.com/download/attachments/23955077/Homepage-categlist.jpg)

---
In order to modify an url or a text, click on Show/Hide Editor and follow the bellow example
This is the default code:
```html
<div class="categlist">
	<div class="background"></div>
	<div class="section">
		<h3 class="categlist__title">Eyewear for the <em>irreverent</em> and <em>slightly</em> jaded.</h3>
		<ul class="flex-wrapper flex list-unstyled categlist__wrapper">
			<li class="flex-item categlist__item"><a href="readers"><i class="icon eb-icon-readers categlist__icon"></i> <strong class="categlist__subtitle">Readers</strong><i class="icon eb-icon-go"></i></a></li>
			<li class="flex-item categlist__item"><a href="allday-readers"><i class="icon eb-icon-allday categlist__icon"></i> <strong class="categlist__subtitle">All Day Readers</strong><i class="icon eb-icon-go"></i></a></li>
			<li class="flex-item categlist__item"><a href="sunglasses"><i class="icon eb-icon-sunglasses categlist__icon"></i> <strong class="categlist__subtitle">Sunglasses</strong><i class="icon eb-icon-go"></i></a></li>
			<li class="flex-item categlist__item"><a href="sunreaders"><i class="icon eb-icon-sunreaders categlist__icon"></i> <strong class="categlist__subtitle">Sunreaders</strong><i class="icon eb-icon-go"></i></a></li>
		</ul>
	</div>
</div>
```

To change the section title edit the content of `<h3>` tag.
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Original Value"]
```<h3 class="categlist__title">Eyewear for the <em>irreverent</em> and <em>slightly</em> jaded.</h3>```
[/ui-tab]
[ui-tab title="Updated Value"]
```<h3 class="categlist__title">ADD YOUR TEXT HERE</h3>```
[/ui-tab]
[/ui-tabs]
[notice]
**Italic text**<br>
In order to add italic text, just wrap the word in an `<em></em>` tag. E.g: `<h3 class="categlist__title">This text is <em>italic</em></h3>`
[/notice]


To change a link, just change the value of href, it's content will be added after the base url (www.eyebobs.com)
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Original Value"]
```<li class="flex-item categlist__item"><a href="readers"><i class="icon eb-icon-readers categlist__icon"></i> <strong class="categlist__subtitle">Readers</strong><i class="icon eb-icon-go"></i></a></li>```
[/ui-tab]
[ui-tab title="Updated Value"]
```<li class="flex-item categlist__item"><a href="INSERT YOUR URL HERE"><i class="icon eb-icon-readers categlist__icon"></i> <strong class="categlist__subtitle">Readers</strong><i class="icon eb-icon-go"></i></a></li>```
[/ui-tab]
[/ui-tabs]


To change the name of a category, modify the content of the `<strong>` tag.
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Original Value"]
```<li class="flex-item categlist__item"><a href="readers"><i class="icon eb-icon-readers categlist__icon"></i> <strong class="categlist__subtitle">Readers</strong><i class="icon eb-icon-go"></i></a></li>```
[/ui-tab]
[ui-tab title="Updated Value"]
```<li class="flex-item categlist__item"><a href="readers"><i class="icon eb-icon-readers categlist__icon"></i> <strong class="categlist__subtitle">INSERT TEXT HERE</strong><i class="icon eb-icon-go"></i></a></li>```
[/ui-tab]
[/ui-tabs]
