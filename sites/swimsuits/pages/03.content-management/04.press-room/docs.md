---
title: Press Room
taxonomy:
    category: docs
---

[ui-browser address="https://swimsuitsdirect.com/press-room"]
![Press Room](https://wiki.rocketweb.com/download/attachments/28279300/press-room-page.png)
[/ui-browser]

To edit Press Room page:
1. Go to `Admin > Content > Pages`
2. Find page with `id="press-room"` and open
3. Turn off Wysiwyg Editor for "Content" textarea
4. Each year starts with heading: ```<h3>[year]</h3>```.

After that there is a wrapper block with articles. 
`<div class="post-grid row">[article1][article2]...[articleN]</div>`

All [article] have the same skeleton:
```html
<div class="col-sm-6 col-xs-12 col">
    <div class="post-holder">
        <div class="post-banner">
            <img
                title="Image title" src="image_url" alt="image alt" width="960" height="624" />
        </div>
        <div class="post-header">
            <h5>Magazine Title</h5>
            <h4 class="h6">
                <a title="Product title" href="{{store url="product_url"}}">Product Name</a>
            </h4>
            <p class="">Post date</p>
        </div>
    </div>
</div>
```

Year Block skeleton:    
```html 
<h3>[year]</h3>
    <div class="post-grid row">

    [Article Skeleton 1]

    [Article Skeleton 2]

    ....

    [Article Skeleton n]
</div>
```
>>> The above markup structure (HTML tags) should not be modified

5. If you want to create a new article, for example in 2013 year, just add the 'Article Skeleton' right after this 2 rows:

```html
<h3>2013</h3>

<div class="post-grid row>
```

and edit the content

To Create new year block the 'Year Block Skeleton' after first `<p>...</p>`:

```html
<h3>2017</h3>

<div class="post-grid row>

</div>
```

