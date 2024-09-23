# TASC

Tasc is a simple, proprietary cutscene scripting language for [Renaine](https://renainegame.com/).

## Features

This extension covers basic formatting and code hinting in VSCode, the basic structure of a .tasc file is:
```
my-entity.myAction(arg1, arg2)
otherAction(arg)
```

There's a small list of valid functions, an invalid function name will highlight a different color, indicating a user typo.

## To-Do

- Actual code completion, rather than just word hinting
- Release the actual TASC parser, created in [Haxe](https://haxe.org/)
- Add images to readme