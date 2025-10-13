# Theming

This page serves as a basic outline on the stock OS's (and in turn Quark's) theme layout.

Feel free to use the [default theme](https://github.com/cobaltgit/Quark/blob/main/Themes/Quark) as a template for creating your own themes!

## config.json

This file is stored in the root of the theme directory and stores the name of the theme, as well as data on the fonts used in the theme, their sizes and colours.

```json
// Quark default theme configuration
{
    "name":"Quark", // theme name, displayed in Themes menu
    "font":"Gill Sans MT Bold-95W.ttf", // font used in unfocused main menu items and list interfaces. (apps, gamelists, settings etc.) font path relative to root of theme
    "fontascii":"BPreplayBold.otf", // font used in the title bar, bottom bar and the focused main menu item. font path relative to root of theme
    "fontsize":{
        "title":18, // size of the title bar text (top-left corner in menus)
        "statbar":17, // size of text at the bottom of the screen
        "list":16 // size of text in list interfaces
    },
    "fontcolor":{
        "title":"#FFFFFF", // colour of title text
        "shadow":"#000000", // colour of drop shadow of title text 
        "statbar":"#FFFFFF", // colour of text in bottom bar
        "list":"#FFFFFF", // colour of text in list interfaces
        "listsel":"#000000", // colour of selected item in list
        "iconlist":"#FFFFFF", // colour of main menu entries in carousel/grid mode
        "iconlistsel":"#FF8080", // colour of selected main menu entry in carousel/grid mode
        "notify":"#00FF00", // ??? (used in the app store for selected button)
        "popup":"#FF0000", // colour of script list text when pressing X in a system's gamelist'
        "popupsel":"#0000FF", // colour of selected script in X-menu
        "highlight":"#FF8080", // colour of highlighted main menu entry
        "subtext":"#7f7f7f" // used for descriptions of apps
    }
} 
```

## `skin/` folder

This folder contains theme assets as shown in the UI

Additionally, in Quark v1.6.0 and above, the `skin/` folder can contain a `bootlogo.bmp` file, which is checked when the system theme is changed and updated if present.

## `sound/` folder

This folder contains:

* `click.wav`: played when navigating the user interface, must be an uncompressed WAVE format file with 44100Hz sample rate. Can be toggled separately in Quark v1.6.0 and above
* `bgm.mp3`: MainUI background music. Volume can be adjusted using the *BGM Volume* setting in the Settings menu.
* `boot.wav`: plays on boot before entering MainUI if present. Must be an uncompressed WAVE format file

!!! note
    `boot.wav` is only played in Quark v1.6.0 and above
