# macOS Software Update Command Line Tool

The macOS `softwareupdate` command is a powerful tool that allows you to interact with the system software update mechanism directly from the terminal. The main functions include listing available updates, downloading specific updates, and installing updates.

## Table of Contents
1. [Requirements](#requirements)
2. [How to use](#how-to-use)
3. [Commands](#commands)
4. [Examples](#examples)
5. [Troubleshooting](#troubleshooting)

## Requirements

* macOS operating system.
* Administrator privileges for certain operations. Please note that most operations will require you to use `sudo`, however for demonstration purposes, the examples given here will not include it.

## How to use

To use the `softwareupdate` tool, open Terminal on your macOS and enter the `softwareupdate` command followed by the desired command-line options.

Example: `softwareupdate --list`

This command will list all available updates for your system.

## Commands

### `softwareupdate --list`
List all available updates.

### `softwareupdate --install [args]`
Download and install specified updates. Args can be:

- `--recommended`: All updates that are recommended for your system.
- `--os-only`: Only macOS updates.
- `--safari-only`: Only Safari updates.
- `--all`: All updates that are applicable to your system, including non-recommended ones.
- `item...`: One or more specified updates.

### `softwareupdate --list-full-installers`
List the available macOS installers.

### `softwareupdate --fetch-full-installer [--full-installer-version]`
Install the latest recommended macOS installer. Specify version with `--full-installer-version`.

### `softwareupdate --install-rosetta`
Install Rosetta. Only applies to Apple silicon Macs.

### `softwareupdate --download [args]`
Download but not install specified updates.

### `softwareupdate --schedule`
Returns the per-machine automatic (background) check preference.

### `softwareupdate --help`
Print command usage.

## Examples

### List available updates

```
softwareupdate --list
```

### Install a specific update

```
softwareupdate --install ProAppsQTCodecs-1.0
```

### Install all recommended updates

```
softwareupdate --install --recommended
```

### Install all applicable updates

```
softwareupdate --install --all
```

### Install only macOS updates

```
softwareupdate --install --os-only
```

### Download, but do not install, a specific update

```
softwareupdate --download ProAppsQTCodecs-1.0
```

### Check automatic update preference

```
softwareupdate --schedule
```

### List full macOS installers

```
softwareupdate --list-full-installers
```

### Fetch and install the latest macOS installer

```
softwareupdate --fetch-full-installer
```

### Fetch and install a specific version of macOS installer

```
softwareupdate --fetch-full-installer --full-installer-version 10.15
```

### Install Rosetta on Apple Silicon Mac

```
softwareupdate --install-rosetta
```

## Troubleshooting

If you encounter any issues while using the `softwareupdate` command, ensure you have entered the command correctly. The command names and arguments are case-sensitive. Also, some operations require administrator privileges so ensure you are using `sudo` where necessary.

Additionally, ensure your system is connected to the internet as the tool requires a connection to check and fetch updates from Apple's servers. If you are still experiencing issues, consider checking Apple's official documentation or community support forums for more information.