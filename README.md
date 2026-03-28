# Language Configuration for ObjectScript CSPs

The [InterSystems ObjectScript Extension](https://marketplace.visualstudio.com/items?itemName=intersystems-community.vscode-objectscript) provides language support for
classes and routines, but not Caché Server Pages.

This extension implements a language configuration for them, adding expected features like auto-closing brackets and quotes.

![Demo of auto-closing brackets, parantheses, quotes, and #server()](https://github.com/ThomasKoppens/cache-csp-formatter/blob/main/assets/function-demo.gif)

## Features

- **Auto-closing** brackets and quotes, as well as `#()#,` `#server()`, and `#call()`
- **Wrapping** code with brackets
- **Smart Indentation**: Indenting on enter in for loops, if statements, HTML tags, etc.
- **Comment toggling**: Commenting out a code line or block with <kbd>Ctrl</kbd> + <kbd>/</kbd>


## Requirements

This extension is designed to work alongside the official [InterSystems ObjectScript Extension](https://marketplace.visualstudio.com/items?itemName=intersystems-community.vscode-objectscript).

## Recommendations

For auto-closing tags, it is recommended to install [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag). To enable support for CSP files, follow these steps:

1. Press <kbd>Ctrl</kbd> + <kbd>,</kbd>
2. Enter `auto-close-tag` in the search bar
3. Find **Auto-close-tag: Activate On Language**
4. Click **Edit in settings.json**
5. Add `"objectscript-csp"` to the list

    <img alt="Auto Close Tag: Activate on Language setting" src="https://github.com/ThomasKoppens/cache-csp-formatter/blob/main/assets/auto-close-activate.png" style="width: 35rem;">

### Preventing Auto-closing of Specific Tags

In some cases, such as `CSP:CLASS`, the tag is not meant to be closed.  To prevent
the default behaviour, you can exclude them in the settings.

Follow steps 1-2 above and then:

1. Find **Auto-close-tag: Excluded Tags**
2. Click **Edit in settings.json**
3. Add the tag to the list (**IMPORTANT:** the tag needs to be lowercase to work)

    <img alt="Auto Close Tag: Excluded Tags setting" src="https://github.com/ThomasKoppens/cache-csp-formatter/blob/main/assets/auto-close-exclude.png" style="width: 35rem;">