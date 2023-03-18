+++
title = "Changelog"
weight = 4
+++

# [0.2.9]

## New features

- announcement bar, configuration view in [configure#options-of-announcement_file](@/configure.md#options-of-announcement-file)
- supporting multilingualism, more at [configure#options-in-config.toml-under-the-languages](@/configure.md#options-in-config-toml-under-the-languages)

## Maintenance
- replacement "$base_url" variable in header setting, to "@" symbol.
- rewrite [configure](@/configure.md) page, and more detailed documentation
- switch to [zola-bin](https://www.npmjs.com/package/zola-bin) in package scripts
- mobile header is sticky position
- folio macros not only the page
- header setting can now be contained in a separate file, more at [configure#options-of-header_file](@/configure.md#options-of-header-file)
- footer remove default settings and move `extra.version` in `[[extra.footer]]`

## Bug fixing

- header right links rendering as a vector
- search icon not displayed in light theme

# [0.2.8]

## New features

- returned search and made for mobile
- page with search results
- clear search input button
- disable children in page with `disable_children` parameter

## Maintenance
- header section is active in the section pages

## Bug fixing
- corrected layout of page navigation

# [0.2.7]

## New features
- diagrams [reference/markdown-syntax#mermaid](@/reference/markdown-syntax.md#mermaid) with shortocode using [mermaid](https://mermaid-js.github.io/mermaid/#/)
- resize images, implementation of [Image processing | Zola](https://www.getzola.org/documentation/content/image-processing/)

## Maintenance
- minor changes in mobile page, fixed header and nav for open menu
- remove script for fetch releases and change to zola load data
- improve code blocks


# [0.2.6]

## New features
- hint shortcode [reference/markdown-syntax#hints](@/reference/markdown-syntax.md#hints)
- anchors for quick page navigation, implementation of [Internal links & deep linking | Zola](https://www.getzola.org/documentation/content/linking/#anchor-insertion)
- edit the page, the path to content repository is configured with `repo` and branch `repo_branch`
- added second-level headings for table of contents

## Maintenance
- disable search and remove js file
- adding prefetch for cdnurl
- improved work with importing scripts using macros
- page layout switch flex to grid
- enable updates macros as a default


# [0.2.5]

## New features
-  dark mode and auto-mode added

## Maintenance
- temporal deprecation taxonomies
- minor changes design in mobile 404 
- moved to typescript
- change a little directory structure in sass folder
- little change design in footnote

## Bug fixing 
- fixed location of footer

# [0.2.4]

## Maintenance
- the theme is fully translated into classless css
- change github workflows to only build
- redesigned search bar 

# [0.2.3]

## New features
- created a container image for the theme and is available `ghcr.io/kogeletey/karzok`

## Maintenance
- began to shift the topic to a paradigm classless
- new url for demonstration theme [karzok](https://karzok.re128.org)


# [0.2.2]

## New features
- new parameter `item.alt` text for your svg icon in header, if it is not specified, then the link to the resource is used as it

## Fix

- adding aria labels, where they were not
- provide zola description by meta tag in html

## Maintenance
- change h3 to span in toc
- change license at the MIT

# [0.2.1]

## New features

- added the ability to tear down the sidebar menu

## Maintenance

- switch from sr.ht builds to github workflows 
- setup staging domain
- README.md remove deprecated parameter and karzok configuration adding link
- Rename src to layout folder, and started common styles into individual components.


# [0.2.0] 

## New features

- mobile version is made in early version
- alpha search
- new settings `relative_path` which prints in full page
- new parameter `config.extra.theme_color` which allow tab coloring in safari
- experimental settings `header.container` activate by `devmode`
- new Dockerfile
- setup postcss and swc to compiling

## Bug fixing

- fixed favicons
- fixing toc and sidebar overflow
- fixing article.css large list
- correct minutes word
- fix bug with typo


## Maintenance

- improved normalize.css by @sindresorhus
- separate header parameter to `header_right` and `header_left`
- README.md set link center and add design with penpot
- remove static folder, by it generation
- .build.yml new steps added for compile and optimize css code
- split the css files and reduced the size of the loaded content
- redesigned menu 
- replaces font with inter
- write components a bem methology
- globally set img width
- separate macros file

# [0.1.3]

## New features

- settings `show_word_count` and `show_reading_time` allowing you to show the
  number of words and the time of reading it on the page, respectively.
- macro toc now has the opinion `config.extra.children` display all headers,
  nested within each other.
- added the ability to set an icon in the header.
- add possibility disable config.menu
- macros new katex contrib plugins added for rendering shortcodes

## Bug fixing

- macro footer now automatically affixes the version, toc trying to highlight a
  specific header on pages
- macros fixed display, now tags are displayed correctly

# [0.1.2]

## New features

- 404 template stylized
- configure the ability to store assets on another cdn.

## Maintenance

- base.html move link to resources for convience from scss file

## Bug fixing

- Sidebar selected in separated files and fix big sidebar error
- Fixed chevron link
- Sidebar width fixing size
- Fixed a bug that manifests itself in the sidebar
- toc fixed width layout error

# [0.1.0]

- new zola theme for your documentation, first public release under license
  Apache 2.0
