# docker-masquerade

docker-masquerade is a collection of shim scripts that run commands in docker containers instead of natively. This makes it easier to move into a new machine - install the ZSH plugin, and `docker` will automagically download the container image the first time you use a given shim script.

## Contents

| Name              | Description                          | Credits          |
| ----------------- | ------------------------------------ | ---------------- |
| `c-mosquitto_pub` | Runs `mosquitto_pub` in a container. | Mine             |
| `c-mosquitto_sub` | Runs `mosquitto_sub` in a container. | Mine             |
| `c-influxdb`      | Run `influxdb` tool in a container.  | Mine             |

## Installation

### Pre-requisites

You must have `docker` installed on your machine to use the tool scripts in this repository.

### zgen

If you're using [zgen](https://github.com/tarjoilija/zgen):

1. Add `zgen load unixorn/docker-masquerade` to your `.zshrc` along with your other `zgen load` commands.
2. `zgen reset && zgen save`

### Antigen

If you're using [Antigen](https://github.com/zsh-users/antigen):

1. Add `antigen bundle unixorn/docker-masquerade` to your `.zshrc` where you've listed your other plugins.
2. Close and reopen your Terminal/iTerm window to **refresh context** and use the plugin. Alternatively, you can run `antigen bundle unixorn/docker-masquerade` in a running shell to have `antigen` load the new plugin.

### oh-my-zsh

If you're using [oh-my-zsh](github.com/robbyrussell/oh-my-zsh):

1. In the command line, change to _oh-my-zsh_'s custom plugin directory :

    `cd ~/.oh-my-zsh/custom/plugins/`

2. Clone the repository into a new `docker-masquerade` directory:

    `git clone https://github.com/unixorn/docker-masquerade.git docker-masquerade`

3. Edit your `~/.zshrc` and add `docker-masquerade` – same as clone directory – to the list of plugins to enable:

    `plugins=( ... docker-masquerade )`

4. Then, restart your terminal application to **refresh context** and use the plugin. Alternatively, you can source your current shell configuration:

    `source ~/.zshrc`

### Bash / Manual Installation

Nothing here actually requires you to use ZSH or zgen, that's just a convenient distribution method for anyone using a ZSH framework.

If you aren't using any ZSH frameworks, or if you're using `bash`, `fish` or another shell, do the following steps:

1. `git clone` this repository
2. Add `cloneDirectory/bin` to your `$PATH` in your shell's startup file.
