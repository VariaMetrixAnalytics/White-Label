# White-Label
VariaMetrix is a tool for professional dashboard development,
expert-driven reporting insights, and creative ad design.

# Table of contents
- [Getting Started](#getting-started)
- [Styles](#styles)
- [Assets](#assets)
- [Components](#components)
- [Installation](#installation)


# Getting Started

The fastest way to begin is to clone this repository and replace the
assets and styles in-place.

The core of your theme is the package.varia.json file which lets
VariaMetrix know what assets to look for and replace.

```json
{
    "name": "Sample Package name",
    "version": "1.0.1",
    "author": "VariaMetrix Devs <devs@variametrix.com> (https://variametrix.com)",
    "license": "MIT",
    "assets": [
      "asset-override/",
    ],
    "styles": [
      "css-override/"
    ],
    "components": [
      {
        "chartblock": [
          {
            "type": "color-palette",
            "path": "components/chartblock/color-palette/color-palette.json"
          }
        ]
      }
    ]
}
```

# Assets

The `assets` array includes search paths for all the images that will be
used in your theme. The default directory is `asset-override/`, but
you can create your own directories to organize assets as you see
fit. If you use the default [CSS rules](#styles) in this repository,
you can simply replace the image files as you see fit.

VariaMetrix supports the following asset formats:
  - .apng
  - .bmp
  - .gif
  - .ico
  - .cur
  - .jpg
  - .jpeg
  - .jfif
  - .pjp
  - .png
  - .svg
  - .tif
  - .tiff


# Styles

The `styles` array contains search paths for any CSS files that will
override the default VariaMetrix stylesheets. The default CSS file is
`css-override/varia-default.css`, which you can modify in-place, but
you can create your own as well.

Keep in mind that the default VariaMetrix CSS file is always loaded
first, then overridden by any stylesheets in your package. They are
loaded in the order they're listed in the `styles` array; if you
specified a directory, files are loaded alphabetically. Like with all
CSS, the last-loaded rules take precedence over rules loaded earlier.

If you use a different scheme for naming asset files than the
VariaMetrix default, you will need to create CSS rules to reference
the new filenames. Assets paths in css must be relative to your
package.varia.json file and path must be prefixed with
`{{varia-url}}`.

## Example:

```css
--navbar-primary-brand-background: url('{{varia-url}}assets/images/varia-logo-title.svg') center no-repeat;
```

# Components

The `components` array allows you to customize chart blocks and other
plug-in components. Currently, only the default chart colors can be
overridden.

## Color Palette

In `package.varia.json`, define the location of your color palette JSON file.

```JSON
{
  "chartblock": [
    {
      "type": "color-palette",
      "path": "components/chartblock/color-palette/color-palette.json"
    }
  ]
}
```

In `color-palette.json` (or other path defined in
`package.varia.json`), create a `colorPalette` array with hex colors
as strings. The color at index 0 will be the default color for all
charts.

```JSON
{
    "colorPalette" : [
        "#321325",
        "#5F0F40",
        "#9A031E",
        "#CB793A",
        "#FCDC4D",
        "#1cc4ae"
    ]
}
```

# Installation

Compress your updated files into a single ZIP archive. You must
include the `package.varia.json` file, but should omit the .git
directory and README.md file.

Sign in and upload your archive at
[https://dashboard.variametrix.com/manage/white-label/package](https://dashboard.variametrix.com/manage/white-label/package)
