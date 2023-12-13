**This fork of
[jeffkreeftmeijer/vim-dim](https://github.com/jeffkreeftmeijer/vim-dim)
contains fixes that work with neovim's updated default colorscheme.
See https://github.com/neovim/neovim/issues/26378 for details.**

# Dim

**Dim** (/dɪm/; a contraction of **Default IMproved**) is a clone of Vim’s default colorscheme, with some improvements:

* It only uses [ANSI colors], so you can assign colors in your terminal emulator yourself
* Syntax highlighting is consistent on light and dark backgrounds

Dim comes with Grim: a monochrome version that limits syntax coloring to grayscales.

[ANSI colors]: https://en.wikipedia.org/wiki/ANSI_escape_code#Colors

## Installation

    git clone --branch 1.x git@github.com:jeffkreeftmeijer/vim-dim.git ~/.vim/pack/plugins/start/vim-dim

After installing, set your `:colorscheme` to `dim` or `grim`.

    " ~/.vimrc
    colorscheme dim

### Pessimistic versioning branches

Dim adheres to [semantic versioning](https://semver.org/spec/v2.0.0.html),
meaning it'll try to keep backwards compatibility in minor and patch releases.
In short:

- A breaking change will bump the _major_ version number (1.0.0 -> 2.0.0)
- An added feature will bump the _minor_ version number (1.0.0 -> 1.1.0)
- A bug fix will bump the _patch_ version number (1.0.0 -> 1.0.1)

Since Vim's plugin manager doesn't allow specifying version ranges, Dim
provides "pessimistic versioning branches" itself to allow users to lock to a
specific version range:

- The branch named `1.x` is updated for every released version in the 1.x range
  (`~> 1.0` or `>= 1.0.0 and < 2.0.0`)
- The branch named `1.1` is updated for every released version in the 1.1.x
  range (`~> 1.1.0` or `>= 1.1.0 and < 1.2.0`)

To install the latest version in the 1.x range, clone Dim's `1.x` branch:

    git clone --branch 1.x git@github.com:jeffkreeftmeijer/vim-dim.git ~/.vim/pack/plugins/start/vim-dim

When updating through `git pull` later, Dim will be updated to any new version,
but not to 2.x.

## Comparison

|                                                                           | `colorscheme default`                                                                              | `colorscheme dim`                                     |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| [wwdc16.terminal]                                                         | ![wwdc16 dark with Vim's default color scheme]![wwdc16 light with Vim's default color scheme]      | ![wwdc16 dark with Dim]![wwdc16 light with Dim]       |
| [appsignal.terminal]                                                      | ![appsignal dark with Vim's default color scheme]![appsignal light with Vim's default color scheme]| ![appsignal dark with Dim]![appsignal light with Dim] |
| Dimmed comments, line numbers, folds, color columns and completion menus. | ![Comments and line numbers in Vim's default color scheme]                                         | ![Comments and line numbers in the Dim color scheme]  |
| Inverted selections                                                       | ![Selections in Vim's default color scheme]                                                        | ![Selections in the Dim color scheme]                 |
| Clear diff coloring                                                       | ![Diff coloring in Vim's default color scheme]                                                     | ![Diff coloring in the Dim color scheme]              |

[wwdc16.terminal]: https://github.com/jeffkreeftmeijer/wwdc16.terminal
[wwdc16 dark with Vim's default color scheme]: https://gist.githubusercontent.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/wwdc16-dark-default.png
[wwdc16 dark with Dim]: https://gist.githubusercontent.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/wwdc16-dark-default2.png
[wwdc16 light with Vim's default color scheme]: https://gist.githubusercontent.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/wwdc16-light-default.png
[wwdc16 light with Dim]: https://gist.githubusercontent.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/wwdc16-light-default2.png

[appsignal.terminal]: https://github.com/jeffkreeftmeijer/appsignal.terminal
[appsignal dark with Vim's default color scheme]: https://gist.githubusercontent.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/appsignal-dark-default.png
[appsignal dark with Dim]: https://gist.githubusercontent.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/appsignal-dark-default2.png
[appsignal light with Vim's default color scheme]: https://gist.githubusercontent.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/appsignal-light-default.png
[appsignal light with Dim]: https://gist.githubusercontent.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/appsignal-light-default2.png

[Comments and line numbers in Vim's default color scheme]: https://gist.githubusercontent.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/numbers-default.png
[Comments and line numbers in the Dim color scheme]: https://gist.github.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/numbers-default2.png
[Diff coloring in Vim's default color scheme]: https://gist.githubusercontent.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/diff-default.png
[Diff coloring in the Dim color scheme]: https://gist.github.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/diff-default2.png
[Selections in Vim's default color scheme]: https://gist.github.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/selection-default.png
[Selections in the Dim color scheme]: https://gist.github.com/jeffkreeftmeijer/0cf01dadd59096853708cd8033b3469c/raw/selection-default2.png
