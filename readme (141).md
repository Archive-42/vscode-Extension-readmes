# HyperTerm Theme

Dark Theme inspired by the simple beautiful design of Hyper Term and Dark++ Italic font ligatures.

## Recommended for best experience

Use [Custom CSS and JS Loader](https://github.com/be5invis/vscode-custom-css) and a font with programming ligature support. [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) has a collection of fonts that have been patched with ligatures they also provide a script which can patch any font.

Dank Mono patched with Nerd Fonts + Operator Mono set with Custom CSS and JS Loader is used in the example below.

| ![Example Code](https://github.com/rubyjasmin/vscode-hyperterm-theme/raw/master/example.png) |
| :--: |
![Theme Screenshot](https://github.com/rubyjasmin/vscode-hyperterm-theme/raw/master/screenshot.png)

## Theme installation

In VScode press `ctrl(⌘) + p` to launch the command palette then run command:

```vscode
ext install rubyjasmin.hyperterm-theme
```

Then press `ctrl(⌘) + k, then press ctrl(⌘) + t`, you will see a theme selection interface. Choose 'Hyper Term Theme'.

## Adding patched fonts like **DankMono Nerd Font + Operator Mono**

### **IMPORTANT: Every major update to VSCode you will need to re-enable Custom CSS and JS**

1. Install [Custom CSS and JS Loader](https://github.com/be5invis/vscode-custom-css)
2. Choose a patched font from [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) or use the Font Patcher to patch any font of your choosing.
3. In VScode press `ctrl(⌘) + ,` to open `User Settings` then add the following options and save changes.

    ```javascript
    {
      ...
      "editor.fontFamily": "DankMono Nerd Font, FuraCode Nerd Font Mono",
      "editor.fontLigatures": true,
      ...
    }
    ```

4. *(optional step)* Add the following to the css file you created for Custom CSS and JS Loader:

    ```css
      .mtki {
        font-family: Operator Mono;
        font-size: 1em;
        font-stretch: ultra-condensed;
      }

      .sidebar {
        border-top: 1px solid rgb(37, 37, 38);
      }
    ```

5. Reload Custom CSS and JS Loader.

## Change log

See [changelog.md](https://github.com/rubyjasmin/vscode-hyperterm-theme/blob/master/CHANGELOG.md)

## Thanks to

- @idbartosz for [Dark++ Italic](https://github.com/idbartosz/vscode-darkpp-italic) "Enhanced VScode Dark+ theme"
- @ryanoasis for [Nerd Fonts](https://github.com/ryanoasis/nerd-fonts) "Iconic font aggregator, collection, & patcher. 3,600+ icons, 50+ patched fonts"
- And of course [Hyper Term!](https://hyper.is)
