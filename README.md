oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![GitHub license](https://img.shields.io/github/license/oclif/hello-world)](https://github.com/oclif/hello-world/blob/main/LICENSE)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g gfh
$ gfh COMMAND
running command...
$ gfh (--version)
gfh/0.0.3 linux-x64 node-v20.9.0
$ gfh --help [COMMAND]
USAGE
  $ gfh COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`gfh hello PERSON`](#gfh-hello-person)
* [`gfh hello world`](#gfh-hello-world)
* [`gfh help [COMMANDS]`](#gfh-help-commands)
* [`gfh plugins`](#gfh-plugins)
* [`gfh plugins:install PLUGIN...`](#gfh-pluginsinstall-plugin)
* [`gfh plugins:inspect PLUGIN...`](#gfh-pluginsinspect-plugin)
* [`gfh plugins:install PLUGIN...`](#gfh-pluginsinstall-plugin-1)
* [`gfh plugins:link PLUGIN`](#gfh-pluginslink-plugin)
* [`gfh plugins:uninstall PLUGIN...`](#gfh-pluginsuninstall-plugin)
* [`gfh plugins:uninstall PLUGIN...`](#gfh-pluginsuninstall-plugin-1)
* [`gfh plugins:uninstall PLUGIN...`](#gfh-pluginsuninstall-plugin-2)
* [`gfh plugins update`](#gfh-plugins-update)

## `gfh hello PERSON`

Say hello

```
USAGE
  $ gfh hello PERSON -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [src/commands/hello/index.ts](https://github.com/gfh/gfh/blob/v0.0.3/src/commands/hello/index.ts)_

## `gfh hello world`

Say hello world

```
USAGE
  $ gfh hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ gfh hello world
  hello world! (./src/commands/hello/world.ts)
```

_See code: [src/commands/hello/world.ts](https://github.com/gfh/gfh/blob/v0.0.3/src/commands/hello/world.ts)_

## `gfh help [COMMANDS]`

Display help for gfh.

```
USAGE
  $ gfh help [COMMANDS] [-n]

ARGUMENTS
  COMMANDS  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for gfh.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.2.20/src/commands/help.ts)_

## `gfh plugins`

List installed plugins.

```
USAGE
  $ gfh plugins [--json] [--core]

FLAGS
  --core  Show core plugins.

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ gfh plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/index.ts)_

## `gfh plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ gfh plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -s, --silent   Silences yarn output.
  -v, --verbose  Show verbose yarn output.

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ gfh plugins add

EXAMPLES
  $ gfh plugins:install myplugin 

  $ gfh plugins:install https://github.com/someuser/someplugin

  $ gfh plugins:install someuser/someplugin
```

## `gfh plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ gfh plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

GLOBAL FLAGS
  --json  Format output as json.

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ gfh plugins:inspect myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/inspect.ts)_

## `gfh plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ gfh plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -s, --silent   Silences yarn output.
  -v, --verbose  Show verbose yarn output.

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ gfh plugins add

EXAMPLES
  $ gfh plugins:install myplugin 

  $ gfh plugins:install https://github.com/someuser/someplugin

  $ gfh plugins:install someuser/someplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/install.ts)_

## `gfh plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ gfh plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help      Show CLI help.
  -v, --verbose
  --[no-]install  Install dependencies after linking the plugin.

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ gfh plugins:link myplugin
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/link.ts)_

## `gfh plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ gfh plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ gfh plugins unlink
  $ gfh plugins remove
```

## `gfh plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ gfh plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ gfh plugins unlink
  $ gfh plugins remove
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/uninstall.ts)_

## `gfh plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ gfh plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ gfh plugins unlink
  $ gfh plugins remove
```

## `gfh plugins update`

Update installed plugins.

```
USAGE
  $ gfh plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v4.0.2/src/commands/plugins/update.ts)_
<!-- commandsstop -->
