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
    "editor.tokenColorCustomizations":
    {
        // normal color settings here
        "textMateRules": 
        [
            // tasc specific colorings here
            { "scope": "variable.control.tasc", "settings": { "foreground": "#dbb3ff" } },
            { "scope": "invalid.illegal.tasc", "settings": { "foreground": "#ff90d3" } },
            { "scope": "constant.other.caps.tasc", "settings": { "foreground": "#00FFFF" } }
            { "scope": "constant.numeric.dec.tasc", "settings": { "foreground": "#FF00FF" } }
        ]
    }
}
```

## To-Do

- Actual code completion, rather than just word hinting
- Release the actual TASC parser, created in [Haxe](https://haxe.org/)
- Add images to readme