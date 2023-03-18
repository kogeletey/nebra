+++
title = "Configure"
weight = 2
+++

## Options in config.toml under the `[extra]`

```toml
[extra]
favicon = "favicon.ico"
header.name = "Home"
theme_color = "#000"

math = false
show_word_count = false
show_reading_time = false
relative_path = false
localcdn = false

repo = "path/to/you/repo"
repo_branch = "you_branch"

cdnurl = "https://cdn.jsdelivr.net/npm"
```

### math 
- type: `boolean`
- default: `false`

Rendering math formulas throught [katex](https://katex.org)

### favicon 
- type: `string`
- default: `favicon.ico`

Set path to favicon icon import

### localcdn
- type: `boolean`
- default: `false`

If you want to store all assets on your domain, then enable this setting

### cdnurl
- type: `string`
- default: `https://cdn.jsdelivr.net/npm`

You can customize your url to store assets

### show_word_count
- type: `boolean`
- default: `false`

Allowing you to show number of words

### show_reading_time
- type: `boolean`
- default: `false`

Allowing you to show reading time

### theme_color 
- type: `string`
- available: since(v0.2.0)

Which allow tab coloring in safari

### repo and repo_branch
- available: since(v0.2.6)
- type: `string`

Repository and branch where it content is stored

### relative_path
- available: since(v0.2.0)
- type: `string`

Which prints in full url on the page

### header.name 
- type: `string`
- default: `Home`

You site name instead of an icon

### extra.header_right,extra.header_left
- type: `array of tables`

Set up global links to resources that will be displayed at the top of the page.

Example all parameters:

```toml
[[extra.header_left]]
lang = "en"
text = "link"
svg = 'svg_icon'
link = "@/example"
target = "_blank"
```

#### `lang`
- available: since(v0.2.9)
- type: `string`
- required: `false`

The parameter is needed for multilingual titles

#### `text`
- type: `string`
- required: `true`, if not set `svg`

It's titles of links

#### `svg`
- type: `string`
- required: `true`, if not set `text`

It's icons of links with svg format

#### `target`
- available: since(v0.2.9)
- type: `string`
- required: `false`
- default: `_self`

Open the links of rules [a target](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/a#attr-target), 
specifying `_blank` an arrow is added on link

#### `link`
- type: `string`
- required: `true`

Link to an external or internal resource.

{% hint(style="warning") %}
Since version 0.2.9 `$base_url` for internal links replacements to `@`.
{% end %}

That is internal link in new versions

`link = "@/internal_resource"`

but in old

`link = "$base_url/internal_resource"`

### announcement_file
- available: since(v0.2.9)
- type: `string`

The path to announcement file

### header_file
- available: since(v0.2.9)
- type: `string`

The path to file header options

### other
1. `children`- for header nesting to work

2. `[[extra.menu]]` - the main navigation on the site

## Options of `announcement_file`
File for announcement that are at the very top of the page.

Specify a file with the extension toml.

The name can be anything.

```toml
text = "text"
bg_color = "#FFF"
text_color = "#111"

[[translations]]
lang = "en"
text = "text"
```

### text 
- type: `string`
- required: `true`, if not translations

Describe your announcement message

### bg_color
- type: `string`
- required: `false`
- default: `var(--background)`, black or white depending on theme

You can specify the background color

### text_color
- type: `string`
- required: `false`
- default: `var(--foreground)`, white or black depending on theme

You can specify the text color

### dismissable
- type: `boolean`
- required: `false`
- default: `false`

Adds the ability to close the bar permanently

### translations
- type: `array of tables`

#### `lang`
- type: `string`
- required: `false`

The parameter is needed for multilingual titles

#### `text`
- type: `string`
- required: `true`

Describe your announcement message in the language from the parameter above

## Options of `header_file`

Available in extra, just put in a separate file

### name
Similarly [#header.name](#header-name) 

```toml
name = "Home"
[[ left ]] # or right [[ right ]]
lang = "en"
text = "link"
svg = 'svg_icon'
link = "@/example"
target = "_blank"
```

### left, right 

Similarly  [#extra.header_left](#extra-header-right-extra-header-left)

## Options in config.toml under the `languages`
- available: since(v0.2.9)
- type: `table`

Terms from translations into various languages

```toml
[languages.en]
build_search_index = true

[languages.en.translations]
description = "The theme for launching fast documentation sites"
toc_etp = "Edit this page"
toc_ita = "In this article"
date = "Date"
authors = "Authors"
updated = "Updated"
words = "words"
```

### description

Main description of the project

### toc_eta

Term **edit this page** for table of contents

### toc_ita

Term **in this article** for table of contents

### date

Term **date** for page or section

### authors

Term **authors** for page or section

### updated

Term **updated** for page or section

### words

Term **words** for page or section

## Templates

All pages are extend to the base.html, and you can customize them as need.
