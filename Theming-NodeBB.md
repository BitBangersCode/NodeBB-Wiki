NodeBB is built on [Twitter Bootstrap](twitter.github.com/bootstrap/), which makes theming incredibly simple.

Using [bootswatch/swatchmaker](https://github.com/thomaspark/bootswatch/tree/gh-pages/swatchmaker), customize the default Bootstrap theme and compile it down to an appropriate CSS file (optionally minified).

## Packaging for NodeBB

NodeBB expects any installed themes to be found in the `/public/themes` folder. Each individual theme has their own folder here.

The theme's folder contain the following files:

* One of `bootstrap.min.css`, `bootstrap.css`, or `style.css`
* theme.json

## `theme.json`
The theme configuration file is a simple JSON string containing all appropriate meta data regarding the theme. Please take not of the following properties:

* `id`: A unique id for a theme (e.g. "my-theme")
* `src`: The filename (in the same folder) that should be interpreted by NodeBB as the theme CSS
* `name`: A user-friendly name for the theme (e.g. "My Theme")
* `description`: A one/two line description about the theme (e.g. "This is the theme I made for my personal NodeBB")
* `screenshot`: A filename (in the same folder) that is a preview image (ideally, 370x250, or an aspect ratio of 1.48:1)
* `url`: A fully qualified URL linking back to the theme's homepage/project