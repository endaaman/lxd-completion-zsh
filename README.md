# lxd-completion-zsh

A [zsh](http://zsh.org) completion for `lxc` command of [LXD](https://linuxcontainers.org/lxd/).

## Installation

### [Antigen](https://github.com/zsh-users/antigen)

```sh
antigen bundle endaaman/lxd-completion-zsh
```

### [zplug](https://github.com/zplug/zplug)

```sh
zplug 'endaaman/lxd-completion-zsh'
```

### Manually

Put `_lxc` file into `$fpath` directory (e.g. defining `fpath=(~/.zsh/completion $fpath)`, place it in `~/.zsh/completion`)

## TODOs

- subcommands completion
  - image
  - init
  - launch
  - move
  - operation
  - publish
  - query
  - rename
  - storage

- list completion
  - profile list
  - snapshot list
  - storage list
  - network list
  - operation list

## License

MIT
