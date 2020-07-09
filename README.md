# White-Label

# Table of contents
<ul>
    <li>Getting Started</li>
    <li>Examples</li>
    <li>Documentation</li>
    <li>Testing</li>
</ul>


# Getting Started 

<h5>package.varia.json Structure</h5>
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
            "type": "color-pallete",
            "path": "components/chartblock/color-palette/color-palette.json"
          }
        ]
      }
    ]
}
```

<ul>
    <li>name - the name of the package.</li>
    <li>version - package version.</li>
    <li>author - author of the package</li>
    <li>license - license type of the package</li>
    <li>assets - containing path of assets to add in the package. See more in documentation</li>
    <li>styles - An array of styles to add in varia metrix package. Package only supports plain CSS file. See more in documentation.</li>
    <li>components - containing a list of customizable component in VariaMetrix. See more in documentation.</li>
</ul>

<h5>Installing package in VariaMetrix</h5>
<ol>
    <li>Clone the package folder</li>
    <li>Compress the files inside package folder, ensure `package.varia.json` is there</li>
    <li>Go to <a href="http://localhost:4200/manage/white-label/package">Package page</a> and upload your compressed file</li>
<ol>

# Testing
<p>To test the styles changes you've made in realtime, In variametrix site, Inspect site elements, In inherited from html section, you'll see all CSS variable we'
ve used in variametrix. You can alter that accordingly. </p>