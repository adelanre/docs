---
description: Access and use Timber from your command line
---

# CLI

Timber integrates with the command line through the [`timber` command line utility](https://github.com/timberio/cli), allowing you to access and searching your logs directly from your terminal.

## Features

* [Live-tail & search your logs](../../usage/live-tailing.md)
* [SQL query your logs](../../usage/sql-querying.md)
* List organizations
* [List sources / applications](../../usage/source-management.md)
* Issue authenticated requests to the [Timber API](https://docs.api.timber.io)

## Installation

### Mac OS

```bash
brew tap timberio/brew && brew install timber
```

### Pre-built binaries

Pre-built binaries can be found in the [releases section](https://github.com/timberio/cli/releases) of the [`cli` repository](https://github.com/timberio/cli):

* [Darwin AMD64](https://github.com/timberio/cli/blob/master)
* [FreeBSD AMD64](https://github.com/timberio/cli/blob/master)
* [Linux AMD64](https://github.com/timberio/cli/blob/master)
* [Linux ARM](https://github.com/timberio/cli/blob/master)
* [Linux ARM64](https://github.com/timberio/cli/blob/master)
* [NetBSD AMD64](https://github.com/timberio/cli/blob/master)
* [OpenBSD AMD64](https://github.com/timberio/cli/blob/master)

### Building From Source

Building from source requires the [`go` runtime](https://golang.org/doc/install):

```bash
git clone git@github.com:timberio/cli.git timber
cd timber
go build
./timber help
```

## Updating

### Mac OS

```bash
brew update
brew upgrade timber
```

### Other

Simply remove the `timber` binary and [re-install it](./#installation).

## Usage

Options and flags can be accessed with the `timber help` command:

```text
NAME:
   timber - Command line interface for the Timber.io logging service

USAGE:
   timber [global options] command [command options] [arguments...]

COMMANDS:
     tail, t  Live tails logs
     orgs     List organizations that you are a part of
     apps     List applications that you have access to
     views    List saved views that you have access to (currently only console views are displayed)
     api      Make authenticated requests to the Timber API (http://docs.api.timber.io)
     help, h  Shows a list of commands or help for one command

GLOBAL OPTIONS:
   --debug, -d                Output debug messages [$TIMBER_DEBUG]
   --api-key value, -k value  Your timber.io API key [$TIMBER_API_KEY]
   --host value, -H value     Timber.io host, useful for testing (default: "https://api.timber.io") [$TIMBER_HOST]
   --color-output, -C         Set to force color output even if output is not a color terminal [$TIMBER_COLOR]
   --monochrome-output, -M    Disable color output [$TIMBER_NO_COLOR]
   --help, -h                 show help
   --version, -v              print the version
```

## Guides

This documentation is designed top-down, focusing on the task first and the medium second. Head over to the [Usage section](../../usage/live-tailing.md) to get started. Simply select the "CLI" tab when reading the guides.
