# lxd-completion-zsh

Zsh completion for `lxc` and `lxd` commands of [LXD](https://linuxcontainers.org/lxd/).

![screenshot](http://static.endaaman.me/images/github/lxd-completion.png)

## Installation

### Using a plugin manager (recommended)

This way is recommended. The `lxc` command updates frequently and this repository as its completion does the same. Therefore, using a plugin manager, you can get the immediate updates when I apply them.

[Antigen](https://github.com/zsh-users/antigen)

```sh
antigen bundle 'endaaman/lxd-completion-zsh'
```

[zplug](https://github.com/zplug/zplug)

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
