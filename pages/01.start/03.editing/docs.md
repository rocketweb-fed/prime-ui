---
title: Editing Docs
taxonomy:
    category: docs
---

There are a couple of ways to edit pages in RWDocs:
1. via admin using markdown editor (local/prod)
2. by editing markdown files directly using text editor
3. through GitHub

### How to edit pages via admin

### How to edit markdown pages directly


### How to edit pages through GitHub
1. Go to [https://github.com/rocketweb-fed/rwdocs](https://github.com/rocketweb-fed/rwdocs)
2. Navigate to _sites/project_folder/pages_ and find the page you want to edit
	[notice=note]
	Each page uses the following structure:
	```
	02.some-page
		01.sub-page
			docs.md
		docs.md
	```
	where:
	- the number specifies the order of the page in navigation
	- folder name represents the page URL
	- file name declares the template the page is using, .md extension is for *markdown*
	- page title is specified via 'title' meta attribute inside the file
	[/notice]
3. Open the corresponding markdown file and click on Edit icon
4. Make your changes and commit