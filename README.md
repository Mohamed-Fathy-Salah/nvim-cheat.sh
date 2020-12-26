# nvim-cheat.sh

[cheat.sh](https://github.com/chubin/cheat.sh) integration for neovim.

nvim-cheat.sh provides elegant UI and remove complexity of url handling and
special symbols for users.

## Screenshots

![](https://user-images.githubusercontent.com/26287448/103150075-3e404d00-4796-11eb-9694-a05c0483ddbb.gif)

## Installation

Install with your favorite plugin manager. For example with vim-plug:

```lua
Plug 'RishabhRD/popfix'
Plug 'RishabhRD/nvim-cheat.sh'
```

## Working

The plugin exports 2 commands:

- Cheat
- CheatWithoutComments

Each command accepts 0 or more arguments. Arguments decide the initial prompt
text.

CheatWithoutComments search the query but don't display the (optional) comments.

Example:
```vim
:Cheat
:Cheat cpp reverse number
:CheatWithoutComments
:CheatWithoutComments cpp reverse number
```

First and third command opens the prompt to search with and without comments
respectively.

Second and fourth command opens the prompt with initial prompt text
``cpp reverse number`` to search with and without comments respectively.

## How to query

Plugin behavior is similar to cheat.sh behavior.

The first word should be the language for query. (e.g. cpp)

Rest of words define the query. (e.g. sum of digits)

An example query:

```
cpp sum of digits
```

Try to put the language name matching vim filetype for the corresponding
language. This would also enable syntax highlighting for result.
Example: using ``javascript`` for javascript language would produce syntax
highlighting. However, using ``js`` for javascript would not as vim recognise
``javascript`` as filetype not ``js``.

For having different results for the same query append \1,  \2, etc to query similar to
classic cheat.sh.

Example: ``cpp read file\1``
