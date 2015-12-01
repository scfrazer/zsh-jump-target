# zsh-jump-target

zsh-jump-target is a ZLE widget for quickly jumping to a spot in a command
line, inspired by Vim's [EasyMotion][easy-motion] and Emacs' [avy][avy] and
[ace-jump-mode][ace-jump-mode].

[easy-motion]: https://github.com/easymotion/vim-easymotion
[avy]: https://github.com/abo-abo/avy
[ace-jump-mode]: https://github.com/winterTTr/ace-jump-mode

###Installation

Clone the git repository:

```zsh
$ git clone https://github.com/scfrazer/zsh-jump-target.git
```

Copy `functions/jump-target` to a directory in your `fpath` and autoload it:

```zsh
autoload -Uz jump-target
zle -N jump-target
```

###Usage

Bind some key to `jump-target`:

```zsh
bindkey "^J" jump-target
```

When you want to jump to a particular spot in a command line, press the bound
key and it will prompt you for a character.  For example, if you wanted to
jump to the beginning of this sentence, you would press capital `F`.  All the
captial `F`'s in the command line will be overlaid with target letters.  Press
the target letter you want and your cursor will jump to that spot.

###Options

`ZSH_JUMP_TARGET_CHOICES` is a string of characters that will be used to mark
targets.  By default it is `a` through `z` and `A` through `Z`.

`ZSH_JUMP_TARGET_STYLE` is the style used to highlight targets.  By default
they will be red, bold, and underlined.
