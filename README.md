QUICK START:

`.vscode/extensions/extension-name`

```
extension-name
|   themes
|   |   theme.json
|   icon.png
|   package.json
```

`package.json`

```json
{
   "name": "custom-theme",
   "version": "1.0.0",
   "publisher": "rangarajanpraneeth",
   "engines": {
      "vscode": "^1.80.0"
   },
   "displayName": "Slate",
   "description": "Custom theme",
   "contributes": {
      "themes": [
         {
            "label": "Slate",
            "uiTheme": "vs-dark",
            "path": "./themes/theme.json"
         }
      ]
   },
   "icon": "./icon.png"
}
```

Visual Studio Code -> `Ctrl + Shift + P` -> `Developer: Install Extension from Location...`

Select `extension-name` folder containing `package.json`

I have found the editor settings in my ```settings.json``` to provide the best overall visual coherence with this theme. They are not required, but I recommend using them for the intended appearance and experience.

![preview](preview.png)

Code shown in the preview was sourced from [cactus-josh](https://github.com/josh-frank/cactus-josh)

```jsonc
// these were added on later
"minimap.selectionOccurrenceHighlight": "#8091aa40" // has some weird alpha layering
"minimapSlider.background": "#00000040"
"minimapSlider.hoverBackground": "#00000040"
"minimapSlider.activeBackground": "#00000040"

// this was removed from the "CSS ID, Selector" section
"meta.selector.css" // class parameters, property names before confirmation
```
