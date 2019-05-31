---
title: Notice
taxonomy:
    category: docs
---

A useful shortcode that performs a similar job to the [markdown-notices](https://github.com/getgrav/grav-plugin-markdown-notices) plugins, allows you to easily create simple notice blocks as seen on http://learn.getgrav.org and http://getgrav.org.  To use simply use the following syntax:
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Shortcode"]
[raw]
```
[notice]
Your **Markdown** text that will appear in the notice
[/notice]
```
[/raw]
[/ui-tab]
[ui-tab title="Output"]
[notice]
Your **Markdown** text that will appear in the notice
[/notice]
[/ui-tab]
[/ui-tabs]



You can also specifically choose from `note`, `info`, `warning`, `tip` types which provide unique color options:
[ui-tabs position="top-left" active="0" theme="lite"]
[ui-tab title="Shortcode"]
[raw]
```
[notice=warning]
Danger Will Robinson! Danger, Will Robinson!
[/notice]
```
[/raw]
[/ui-tab]
[ui-tab title="Output"]
[notice=warning]
Danger Will Robinson! Danger, Will Robinson!
[/notice]
[/ui-tab]
[/ui-tabs]
