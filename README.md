# TASC

Tasc is a simple, proprietary cutscene scripting language for [Renaine](https://renainegame.com/).

This extension was made by modifying [intcode](https://github.com/benediktwerner/intcode) by [benediktwerner](https://github.com/benediktwerner) (Thanks!)

## Features

This extension covers basic formatting and code hinting in VSCode, the basic structure of a .tasc file is:
```
my-entity.myAction(arg1, arg2)
otherAction(arg)
```

There's a small list of valid functions, an invalid function name will highlight a different color, indicating a user typo.

Here's an example of some color customizations in your settings.json:
```json
{
    "editor.tokenColorCustomizations": {
        "variables": "#EEEEFF",
        "strings": "#FF4080",
        "comments": "#008040",
        "functions": "#88CCFF",
        "numbers": "#FFFF00",
        "textMateRules": [
            { "scope": "variable.control.tasc", "settings": { "foreground": "#eeeeff" } },
            { "scope": "keyword.operator", "settings": { "foreground": "#909090" } },
            { "scope": "keyword.control", "settings": { "foreground": "#FF0000" } },
            { "scope": "keyword.other", "settings": { "foreground": "#FF0000" } },
            { "scope": "invalid.illegal", "settings": { "foreground": "#ff90d3" } },
            { "scope": "constant.other.caps", "settings": { "foreground": "#0000FF" } }
        ]
    }
}
```

## To-Do

- Actual code completion, rather than just word hinting
- Release the actual TASC parser, created in [Haxe](https://haxe.org/)
- Add images to readme