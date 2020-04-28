---
title: Tables
taxonomy:
    category: docs
---

Tables are created by adding pipes as dividers between each cell, and by adding a line of dashes (also separated by bars) beneath the header. Note that the pipes do not need to be vertically aligned.


```markdown
| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
```

Renders to:

| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

And this HTML:

```html
<table>
  <tr>
    <th>Option</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>data</td>
    <td>path to data files to supply the data that will be passed into templates.</td>
  </tr>
  <tr>
    <td>engine</td>
    <td>engine to be used for processing templates. Handlebars is the default.</td>
  </tr>
  <tr>
    <td>ext</td>
    <td>extension to be used for dest files.</td>
  </tr>
</table>
```

### Right aligned text

Adding a colon on the right side of the dashes below any heading will right align text for that column.

```markdown
| Option | Description |
| ------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |
```

| Option | Description |
| ------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |
| ext    | extension to be used for dest files. |

---
## Importing table from a file
We've installed an extension that allows to import tables from a CSV, JSON or YAML files and convert them into HTML code. See usage instructions below for more details.

### Formatting Your Data

The plugin is naive and assumes that your data is well formed and that your tables have even row lengths (the table is rectangular). If the plugin can't find the data file or can't understand its format, then the shortcode will be replaced by an error message. Otherwise, the only evidence something is wrong will be the shortcode still showing or weird table rendering.

The only requirement is that your data file parse to a two-dimensional array: an array of rows from top to bottom, each row containing cells from left to right. Each cell must be a value PHP can natively render as a string.

Some samples—json, then yaml, then CSV:

```json
[
  ["Col1", "Col2", "Col3"],
  ["Val1", "Val2", "Val3"],
  ["Val4", "Val5", "Val6"],
  ["Val7", "Val8", "Val9"]
]
```

```yaml
-
  - Col1
  - Col2
  - Col3
-
  - Val1
  - Val2
  - Val3
-
  - Val4
  - Val5
  - Val6
-
  - Val7
  - Val8
  - Val9
```

```csv
Col1,Col2,Col3
Val1,Val2,Val3
Val4,Val5,Val6
Val7,Val8,Val9
```

### Inserting a Table

This plugin uses the [Shortcode Core](https://github.com/getgrav/grav-plugin-shortcode-core) infrastructure. Read those docs for the nitty gritty of how shortcodes work.

The Table Importer shortcode is a self-closing `[ti option1="value1" option2="value2" ... /]`, and it accepts the following options:

* `file` is the only required parameter. It points to the datafile you wish to load. By default, the plugin looks in the same folder as the page file. This is adequate for most usage. You can also load files from the `user/data` folder by prefixing your file name with `data:` (e.g., `file=data:tables/mytable.yaml`). 

  If all you're passing is the file name, then you can shorten the code to the form `[ti=mytable.yaml/]`.

* `type` is usually unnecessary. It tells the plugin what format the data file is in. The only acceptable values are `yaml`, `json`, and `csv`. However, the plugin looks at the file name extension first. If it's `yaml`, `yml`, `json`, or `csv`, then there's no need to use the `type` option. 

* `caption` will insert a `<caption>` tag containing the value of this option after being run through PHP's `htmlspecialchars`.

* `header` tells the plugin whether you want a header row or not. By default, the first row is rendered as a header. Passing *any* value to `header` will disable the header row.

* `class` lets you assign class definitions to the table itself. Whatever you put here will be escaped (via PHP's `htmlspecialchars`) and placed into the opening `<table>` tag.

* By default, the content of each cell is escaped using PHP's `htmlspecialchars` function. If the `raw` option is set to anything at all, the escaping will be disabled. **Only do this if you trust the incoming data!**

* Finally, for CSV files only, you can customize how it will be parsed using any of the following three options:

  * `delimiter` defines how columns are separated. By default, the value is a comma (`,`).

  * `enclosure` defines how cells with special characters are contained. By default, the value is a double quotation mark (`"`).

  * `escape` defines how special characters can be escaped. By default, the value is a backslash (`\`).

### Example Codes
[raw]
* `[ti=test.json]` (basic import of json table in the same folder as the page itself)

* `[ti=data:test.yaml]` (basic import of yaml table in the `user/data` folder)

* `[ti file=json-as-yaml.json type=yaml]` (parse a file as yaml regardless of extension)

* `[ti file=file.csv enclosure=']` (parse a CSV file that uses a single quote to enclose items)

* `[ti file=file.yaml header="false" class="imported"]` (basic yaml table with no header and a class of `imported`)
[/raw]