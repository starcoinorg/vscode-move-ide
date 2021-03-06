# Changelog

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

### [0.4.2](https://github.com/starcoinorg/vscode-move-ide/compare/v0.4.1...v0.4.2) (2020-07-20)


### Features

* upgrade language server ([70b76a6](https://github.com/starcoinorg/vscode-move-ide/commit/70b76a62226c245ad93eb1e534e273964fb54e24))

# Change Log

## v0.4.1

New features:

- Support providing script running arguments from config file.

## v0.4.0

Inital release of Starcoin IDE.

## v0.3.6 - bytestring literal support

- fixes `move` and `copy` highlight
- adds string literals to syntax
- move-runner and move-language server now support win32
- commands are now run in terminal instead of modal (hooray!)
- Libra std is almost latest - just before built-in assert
- `move-build` arguments fixed for latest version


## v0.3.5

- fixes move-executor run command due to recent changes in cli args

## v0.3.4 - `signer` type support in MLS and syntax

- adds highlighting of `signer`  type and `move_to`
- move-language-server also updated to latest v0.8.2 along with move-executor
- Libra stdlib updated to latest version

## v0.3.3 - Syntax is now scope based

- spec syntax support added
- scope-based regexps now only highlight correct statements in correct scope
- fixed few bugs in hl - address type param in generic now works properly
- fixed incorrect property name when using global config

## v0.3.2

- `download-binaries` could fail on some systems - fixed
- dfinance address highlighting fixed
- newest stdlib loaded

## v0.3.0 - Move Runner and improved MLS

###  Features

- Multiple workspaces support - now you can work on multiple projects
- `Move: Run Script` command is now available - it runs an opened script (with dependencies!)
- Config tracking - updates of config file instantly trigger MLS config changes
- Syntax now supports `address {}` and `script {}` blocks

### General

- Move Runner (move-executor) is now supported - you can run your scripts in sandbox mode
- project is now in TypeScript: config interfaces, autocompletion and more safety over built-in types
- multiple workspaces are now supported as new instance of MLS is run for each Move workspace
- dfinance compiler support is temporarily frozen, waiting for new compiler
- code reorganised for proper use of VSCode's built-in interfaces (such as `TextDocument`)
- better support of dialects and dfinance address format

### Configuration

- address input now works correctly and has placeholders for each network
- `move.compilerUrl` removed as dfinance will no longer need it
- `move.languageServerPath` added, now custom MLS binary can be chosen
- `move.moveExecutorPath` added to allow using other versions of move-executor
- `move.defaultAccount` changed to `move.account` - better order
- `move.network` extension setting is now `move.blockchain` - better order

### .mvconfig.json

- changes are now tracked and trigger MLS config update
- now use `sender` instead of `defaultAccount`

### Move

- `script {}` and `address ... {}` blocks are now supported by MLS and IDE
- updated standard libraries to newest versions
- improved syntax highlighting

### Dependencies

- move-language-server is updated to v0.7.0
- move-executor is at v0.7.0
- move-build is now at version 12.05.20


## v0.2.0 - Libra compiler support added and Move Language Server upgraded

- Move Language Server updated to version v0.3.0 and supports dependencies checks
- Libra compiler is built in on Linux and Darwin
- many small bugfixes
- code separation + refactoring in extension.js
- new way of loading binaries in postpublish!