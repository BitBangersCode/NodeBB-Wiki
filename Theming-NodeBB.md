NodeBB is built on [Twitter Bootstrap](twitter.github.com/bootstrap/), which makes theming incredibly simple.

## Packaging for NodeBB

NodeBB expects any installed themes to be installed via `npm`. Each individual theme is an npm package, and users can install themes through the command line:

    e.g. npm install nodebb-theme-modern-ui

The theme's folder must contain at least two files for it to be a valid theme:

1. `theme.json`
1. `theme.less`

`theme.less` is where your theme's styles will reside. NodeBB expects LESS to be present in this file, and will precompile it down to CSS on-demand. For more information regarding LESS, take a look at [the project homepage](http://lesscss.org/).

## `theme.json`
The theme configuration file is a simple JSON string containing all appropriate meta data regarding the theme. Please take note of the following properties:

* `id`: A unique id for a theme (e.g. "my-theme")
* `name`: A user-friendly name for the theme (e.g. "My Theme")
* `description`: A one/two line description about the theme (e.g. "This is the theme I made for my personal NodeBB")
* `screenshot`: A filename (in the same folder) that is a preview image (ideally, 370x250, or an aspect ratio of 1.48:1)
* `url`: A fully qualified URL linking back to the theme's homepage/project