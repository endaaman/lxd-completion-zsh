# lxd-completion-zsh

A [zsh](http://zsh.org) completion for `lxc` command of [LXD](https://linuxcontainers.org/lxd/).

## Installation

### [Antigen](https://github.com/zsh-users/antigen)

```sh
antigen bundle endaaman/lxd-completion-zsh↲
```

### [zplug](https://github.com/zplug/zplug)

```sh
zplug 'endaaman/lxd-completion-zsh'
```

### Manually

Put `_lxc` file into `$fpath` directory (e.g. defining `fpath=(~/.zsh/completion $fpath)`, place it in `~/.zsh/completion`)

## TODOs

- command
  - network
    - network subcommands
    - network list
  - operation
    - operation subcommands
  - profile
    - profile list
  - publish
    - remote list
  - image
    - image list
  - launch/init
    - profile list
    - network list
  - move
    - snapshot list
- module
  - profile list
  - snapshot list

## License

MIT
