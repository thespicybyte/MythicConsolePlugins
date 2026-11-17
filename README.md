# Mythic Console Plugins

Reference plugins for [Mythic Console](https://github.com/thespicybyte/MythicConsole).

Mythic Console supports any Mythic payload type out of the box: it builds each command set from the
server's own command catalog, with no agent-specific code. A plugin adds curation on top of that
baseline — custom commands, output formatting, client-side scripts, and confirmation prompts. The
plugins here are worked examples. Install one as it is, or copy it as the starting point for your
own.

## Plugins

| Plugin | Payload type | Description |
|--------|--------------|-------------|
| [poseidon](poseidon) | `poseidon` | Reference plugin for the [Poseidon](https://github.com/MythicAgents/poseidon) Mythic agent. |

## Install

Install a plugin straight from this repository. Use `--subdir` to pick one:

```shell
mythic-console install https://github.com/thespicybyte/MythicConsolePlugins --subdir poseidon
```

Or clone the repository first and install from the local path:

```shell
git clone https://github.com/thespicybyte/MythicConsolePlugins.git
mythic-console install MythicConsolePlugins/poseidon
```

You can also install from inside the console with `plugin install <url|path>`. List and remove
installed plugins with `mythic-console plugin list` and `mythic-console plugin remove <name>`.

## Write your own

Each plugin is a package with a `manifest.json` and a `PluginAgent` entrypoint. Scaffold a new one
with `mythic-console plugin new <name> <payload-type>`, then follow the customization guide in the
main project:
[customize.md](https://github.com/thespicybyte/MythicConsole/blob/main/customize.md).
