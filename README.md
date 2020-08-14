# lxd-completion-zsh

A [zsh](http://zsh.org) completion for `lxc` command of [LXD](https://linuxcontainers.org/lxd/).

## Installation

### [Antigen](https://github.com/zsh-users/antigen)

```sh
antigen bundle 'endaaman/lxd-completion-zsh'
```

### [zplug](https://github.com/zplug/zplug)

```sh
zplug 'endaaman/lxd-completion-zsh'
```

### [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)


1. Clone this repository in oh-my-zsh's plugins directory:

```sh
git clone https://github.com/endaaman/lxd-completion-zsh ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/lxd-completion-zsh
```

2. Activate the plugin in ~/.zshrc:

```sh
plugins=( [plugins...] lxd-completion-zsh)
```

3. Restart zsh (such as by opening a new instance of your terminal emulator).

### Manually

Put `_lxc` file into `$fpath` directory (e.g. defining `fpath=(~/.zsh/completion $fpath)`, place it in `~/.zsh/completion`)

## License

MIT
