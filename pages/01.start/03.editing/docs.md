---
title: Editing Docs
taxonomy:
    category: docs
---

There are a couple of ways to edit pages in RWDocs:
- [via admin using markdown editor](#admin)
- [by editing markdown files directly on your local using text editor](#files)
- [through GitHub](#github)

<a id="admin"></a>
### How to edit pages via admin 
1. Go to *http://yourlocaladdress.com/project_folder/admin*
2. Log in using your own credentials
3. Navigate to **Pages**
4. Find the page you want to edit
5. Make your changes
6. Save
7. Hit *git* link to sync local with remote
8. Notify RWDocs moderators of your changes so they can review and update if necessary
>>>>>> By allowing moderators to review and approve we make sure the documentation is consistent and readable.

<a id="files"></a>
### How to edit markdown pages directly on your local 
1. Navigate to *root_folder/user/sites/project_folder/pages* and find the page you want to edit
	[notice]
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
	- file name declares template the page is using, .md extension is for *markdown*
	- page title is specified via 'title' meta attribute inside the file
	[/notice]
2. Make your changes
3. Log in to admin
4. Hit *git* link to sync local with remote
5. Notify RWDocs moderators of your changes so they can review and update if necessary

<a id="github"></a>
### How to edit pages through GitHub 
1. Go to [https://github.com/rocketweb-fed/rwdocs](https://github.com/rocketweb-fed/rwdocs)
2. Navigate to *sites/project_folder/pages* and find the page you want to edit
	>>>>> See note in the previous section on how page files are structured.
3. Open the corresponding markdown file and click on 'Edit' icon
4. Make your changes and create a new Pull Request
5. Notify RWDocs moderators of your changes so they can review and update if necessary
