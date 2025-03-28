---
title: tiup cluster help
summary: tiup-cluster provides help information for users in the command line interface. Use the `help` command or `--help` option to access it. Specify `[command]` to view help information for a specific command. The output is the help information of the specified command or tiup-cluster.
---

# tiup cluster help

tiup-cluster provides a wealth of help information for users in the command line interface. You can obtain it via the `help` command or the `--help` option. `tiup cluster help <command>` is basically equivalent to `tiup cluster <command> --help`.

## Syntax

```shell
tiup cluster help [command] [flags]
```

`[command]` is used to specify the help information of which command that users need to view. If it is not specified, the help information of tiup-cluster is viewed.

### -h, --help

- Prints the help information.
- Data type: `BOOLEAN`
- Default: false

## Output

The help information of the `[command]` or tiup-cluster.
