#compdef lxc

_lxc() {
  local context curcontext=$curcontext state line
  declare -A opt_args
  local ret=1

  _arguments -C \
    {--all,--all}'[Print less common commands]' \
    {--help,--help}'[Show help]' \
    {--verbose,--verbose}'[Print verbose information]' \
    {--version,--version}'[Show client version]' \
    '1: :__lxc_commands' \
    '*:: :->args'
  case $state in
    (args)
      case $words[1] in
        (config)
          _arguments -C \
            {--help,--help}'[Show help]' \
            '1: :__lxc_config_commands' \
            && ret=0
            case $words[2] in
              (device)
                _arguments -C \
                  '2: :__lxc_config_device_commands' \
                  && ret=0
                case $words[3] in
                  (add|get|set|unset|list|show|remove)
                    _arguments -C \
                      '3: :__lxc_containers_all' \
                      && ret=0
                    ;;
                esac
                ;;
              (trust)
                _arguments -C \
                  '2: :__lxc_config_trust_commands' \
                  && ret=0
                case $words[3] in
                  (list|add|remove)
                    # complete remote
                    ;;
                esac
                ;;
            esac
          ;;
        (copy)
          _arguments -C \
            {--help,--help}'[Show help]' \
            && ret=0
          ;;
        (delete)
          _arguments -C \
            {--help,--help}'[Show help]' \
            '*: :__lxc_containers_stopped' \
            && ret=0
          ;;
        (exec)
          _arguments -C \
            {--help,--help}'[Show help]' \
            {--debug,--debug}'[Enables debug mode]' \
            {--env,--env}'[An environment variable of the form HOME=/home/foo]' \
            {--force-local,--force-local}'[Force using the local unix socket]' \
            {--mode,--mode}'[Override the terminal mode (auto, interactive or non-interactive)]' \
            {--no-alias,--no-alias}'[Ignore aliases when determining what command to run.]' \
            {--verbose,--verbose}'[Enables verbose mode]' \
            '1: :__lxc_containers_running' \
            && ret=0
          ;;
        (file)
          _arguments -C \
            {--help,--help}'[Show help]' \
            '1: :__lxc_file_commands' \
            && ret=0
          ;;
        (help)
          _arguments -C \
            {--help,--help}'[Show help]' \
            '1: :__lxc_commands' \
            && ret=0
          ;;
        (image)
          _arguments -C \
            {--help,--help}'[Show help]' \
            '1: :__lxc_image_commands' \
            && ret=0
            case $words[2] in
              (alias)
                _arguments -C \
                  '2: :__lxc_image_alias_commands' \
                  && ret=0
            esac
          ;;
        (info)
          _arguments -C \
            {--help,--help}'[Show help]' \
            && ret=0
          ;;
        (launch)
          _arguments -C \
            {--help,--help}'[Show help]' \
            && ret=0
          ;;
        (list)
          _arguments -C \
            {--help,--help}'[Show help]' \
            && ret=0
          ;;
        (move)
          _arguments -C \
            {--help,--help}'[Show help]' \
            && ret=0
          ;;
        (network)
          _arguments -C \
            {--help,--help}'[Show help]' \
            && ret=0
          ;;
        (profile)
          _arguments -C \
            {--help,--help}'[Show help]' \
            && ret=0
          ;;
        (publish)
          _arguments -C \
            {--help,--help}'[Show help]' \
            && ret=0
          ;;
        (remote)
          _arguments -C \
            {--help,--help}'[Show help]' \
            && ret=0
          ;;
        (restart)
          _arguments -C \
            {--help,--help}'[Show help]' \
            '1: :__lxc_containers_running' \
            && ret=0
          ;;
        (restore)
          _arguments -C \
            {--help,--help}'[Show help]' \
            && ret=0
          ;;
        (restart)
          _arguments -C \
            {--help,--help}'[Show help]' \
            '1: :__lxc_containers_running' \
            && ret=0
          ;;
        (snapshot)
          _arguments -C \
            {--help,--help}'[Show help]' \
            && ret=0
          ;;
        (start)
          _arguments -C \
            {--help,--help}'[Show help]' \
            '*: :__lxc_containers_stopped' \
            && ret=0
          ;;
        (stop)
          _arguments -C \
            {--help,--help}'[Show help]' \
            '*: :__lxc_containers_running' \
            && ret=0
          ;;
      esac
      ;;
  esac
  return ret
}

__lxc_commands() {
    local -a _c
    _c=(
      'config:Manage configuration'
      'copy:Copy containers within or in between lxd instances'
      'delete:Delete containers or container snapshots'
      'exec:Execute the specified command in a container'
      'file:Manage files on a container'
      'help:Presents details on how to use LXD'
      'image:Manipulate container images'
      'info:List information on LXD servers and containers'
      'launch:Launch a container from a particular image'
      'list:Lists the available resources'
      'move:Move containers within or in between lxd instances'
      'network:Manage networks'
      'profile:Manage configuration profiles'
      'publish:Publish containers as images'
      'remote:Manage remote LXD servers'
      'restart:Changes state of one or more containers to restart'
      'restore:Set the current state of a resource back to a snapshot'
      'snapshot:Create a read-only snapshot of a container'
      'start:Changes state of one or more containers to start'
      'stop:Changes state of one or more containers to stop'
    )
    _describe -t commands Commands _c
}

__lxc_config_commands() {
    local -a _c
    _c=(
      'device:Manage device config'
      'get:Get container or server configuration key'
      'set:Set container or server configuration key'
      'unset:Unset container or server configuration key'
      'edit:Edit container or server configuration key'
      'trust:Manage certs config'
    )
    _describe -t config_commands 'Config commands' _c
}

__lxc_config_device_commands() {
    local -a _c
    _c=(
      'add:Add a device to a container'
      'get:Get a device property'
      'set:Set a device property'
      'unset:Unset a device property'
      'list:List devices for container'
      'show:Show full device details for container'
      'remove:Remove device from container'
    )
    _describe -t config_device_commands 'Config device commands' _c
}

__lxc_config_trust_commands() {
    local -a _c
    _c=(
      'list:List all trusted certs'
      'add:Add certfile.crt to trusted hosts'
      'remove:Remove the cert from trusted hosts'
    )
    _describe -t config_trust_commands 'Config trust commands' _c
}

__lxc_file_commands() {
    local -a _c
    _c=(
      'pull:Pull file from container'
      'push:Push file to container'
      'edit:Edit file on container'
    )
    _describe -t file_commands 'File commands' _c
}

__lxc_image_commands() {
    local -a _c
    _c=(
      'copy:Copy an image from one LXD daemon to another over the network'
      'delete:Delete one or more images from the LXD image store'
      'export:Export an image from the LXD image store into a distributable tarball'
      'info:Print everything LXD knows about a given image'
      'list:List images in the LXD image store. Filters may be of the'
      'show:Yaml output of the user modifiable properties of an image'
      'edit:Edit image, either by launching external editor or reading STDIN'
      'alias:Manage alias for image in the LXD image store'
    )
    _describe -t image_commands 'Image commands' _c
}


__lxc_file_commands() {
    local -a _c
    _c=(
      'pull:Pull file from container'
      'push:Push file to container'
      'edit:Edit file on container'
    )
    _describe -t file_commands 'Image alias commands' _c
}

__lxc_containers_running () {
    local -a _containers
    _containers=(${(@f)"$(_call_program repositories lxc list --fast | tail -n +4 | awk '{print $2 $4}' | egrep 'RUNNING$' | sed -e "s/RUNNING//")"})
    _describe -t containers 'Running Containers' _containers
}

__lxc_containers_stopped () {
    local -a _containers
    _containers=(${(@f)"$(_call_program repositories lxc list --fast | tail -n +4 | awk '{print $2 $4}' | egrep 'STOPPED$' | sed -e "s/STOPPED//")"})
    _describe -t containers 'Stopped containers' _containers
}

__lxc_containers_all () {
    local -a _containers
    _containers=(${(@f)"$(_call_program repositories lxc list --fast | tail -n +4 | awk '{print $2}' | egrep -v '^(\||^$)')"})
    _describe -t containers 'All containers' _containers
}

compdef _lxc lxc


