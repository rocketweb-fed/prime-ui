---
title: Images
taxonomy:
    category:
        - docs
---
## Syntax

Images have a similar syntax to links but include a preceding exclamation point.

```markdown
![Minion](minion.png)
```
![Minion](http://octodex.github.com/images/minion.png)

or
```markdown
![Alt text](stormtroopocat.jpg "The Stormtroopocat")
```
![Alt text](http://octodex.github.com/images/stormtroopocat.jpg "The Stormtroopocat")

Like links, Images also have a footnote style syntax

```markdown
![Alt text][id]
```
![Alt text][id]

With a reference later in the document defining the URL location:
```
[id]: http://octodex.github.com/images/dojocat.jpg  "The Dojocat"
```


## Where to store images
Usually you'll use a media file within a page, so just put the file in the page folder, and you can reference it in the Markdown of the page, for example:
```
![](image.jpg)
```

If you want to put all your images in a single folder, you can put them in a user/pages/images folder. That way you can reach them via
```
page.find('/images').media['my-image.jpg']
```

and also you can find them easily via markdown and perform operations on them:
```
![](/images/my-image.jpg?cropResize=300,300)
```
Alternatively you can put them in your theme, as that is easily accessible via CSS references.


## Linking to external images
To link to external images simply put the absolute link in place of the file name (between the brackets).
>>> Note that when using external images you cannot take advantage of Grav built-in [Actions](https://learn.getgrav.org/content/media#actions) (lightbox, resize, crop etc.).

## Lightbox
All images can be opened in modal using additional Lightbox module that utilizes [featherlight.js](https://github.com/noelboss/featherlight) jQuery plugin.

### Using Lightbox with hosted images
To implement a lightbox using Featherlight in Grav, you must output the proper HTML output. Luckily Grav already takes care of this for you if you are using Grav media files.

In markdown this could look something like:
```
![Sample Image](sample-image.jpg?lightbox=1024&cropResize=200,200)
```
In Twig this could look like:
```
{{ page.media['sample-image.jpg'].lightbox(1024,768).cropResize(200,200).html('Sample Image') }}
```
More details can be found in the [Grav documentation for Media functionality](http://learn.getgrav.org/content/media).


### Using Lightbox with external images
To open an external image in lightbox a special class `lightbox` needs to be added to image tag via Markdown. The only way to do this is to use traditional img HTML tag. 
```
<img src="http://octodex.github.com/images/dojocat.jpg" alt="Image" class="lightbox" />
```
<img src="http://octodex.github.com/images/dojocat.jpg" alt="Image" class="lightbox" width="200" height="200"  />
