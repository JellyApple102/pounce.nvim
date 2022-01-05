# pounce.nvim

Pounce is a motion plugin similar to [EasyMotion][1], [Sneak][2], [Hop][3],
[Lightspeed][4], and more. It's based on incremental fuzzy search. Here's a
demo:

[![asciicast](https://asciinema.org/a/XPeOoohPKqlazq879FMX07Hl3.svg)](https://asciinema.org/a/XPeOoohPKqlazq879FMX07Hl3)

[1]: https://github.com/easymotion/vim-easymotion
[2]: https://github.com/justinmk/vim-sneak
[3]: https://github.com/phaazon/hop.nvim
[4]: https://github.com/ggandor/lightspeed.nvim

## Installation

Using vim-plug:

```
Plug 'rlane/pounce.nvim'
```

## Usage

The `:Pounce` command starts the motion. Type the character at the
destination and Pounce will highlight all matches on screen. Next, refine
the matches by typing more characters (in order) that are present after the
destination. The fuzzy search algorithm will find the best match which will be
highlighed in green. Other matches will be highlighted in orange. You can hit
enter to accept the match and jump to it, or C-j/C-k to scroll through the
matches. Escape cancels the motion and leaves the cursor at its previous
position.

No mappings are created by default. Here's a suggestion:

```
nmap s <cmd>Pounce<CR>
vmap s <cmd>Pounce<CR>
```