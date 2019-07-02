---
title: Shortcodes
taxonomy:
    category: docs
---

The **Shortcode Core** plugin allows for the development of simple yet powerful shortcode plugins that utilize the common format utilized by **WordPress** and **BBCode**. The core plugin loads the libraries required and fires a new event that other plugins can use.  It also provides a mechanism for adding CSS/JS assets that are cached so that shortcodes can work effectively even when the processed page content is cached.  This ensures that shortcodes are only processed once and will not impact performance by doing unnecessary work on every page.

This plugin uses the [Thunderer Advanced shortcode engine](https://github.com/thunderer/Shortcode). For more information please check out that repo on GitHub.

## Quick Example

This example functionality is provided with the **Shortcode Core** plugin to provide some functionality that is not available in traditional markdown but is standard **BBCode** used in many form platforms.  You can see how the syntax is just a simple open and close element using square brackets.

![Shortcodes example](shortcodes.png)
```markup
[raw]
This is some [u]bb style underline[/u] and not much else

[center]This is centered[/center]

This is [size=30]bigger text[/size] and this is [color=blue]blue text[/color]
[/raw]
```
This will render:
```
This is some [u]bb style underline[/u] and not much else

[center]This is centered[/center]

This is [size=30]bigger text[/size] and this is [color=blue]blue text[/color]
```

The core plugin required for any other shortcode specific plugin. Provides some basic BBCode style syntax such as underline, color, center, and size.