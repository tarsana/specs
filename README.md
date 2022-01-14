# Tarsana

## The Goal

The aim is to have an ecosystem in which developers can build and share command line apps (commands for short).

To acheive this goal, several components are needed:

1. A framework to build commands.
2. A command to create, install and publish commands (like `composer` and `npm`).
3. A public repository to browse and search for commands (like `packagist` and `npmjs.com`).

## The Framework

The PHP language was chosen simply because I wanted to rewrite my [lumen-generators](https://github.com/webNeat/lumen-generators) using this framework. Now I start to consider switching to Javascript...

To build a working version of the framwork, I need the following components:

- `filesystem` to read, write and manipulate streams, files and directories.
- `syntax` to parse structured strings (mainly used to parse command line args).
- `terminal` to read from, write to, and handle interactions on the console.
- `command` to build command line apps and test them easily.

In the process, I built these useful components:

- `functional` because I liked functional programming and [Ramda](http://ramdajs.com)


### [Filesystem](https://github.com/tarsana/filesystem)

- [X] Should create, copy, move and delete files and directories.
- [X] Should list and find files in directories.
- [X] Should read from and write to streams and files.
- [X] Should mock files and directories into memory (useful for testing).


### [Syntax](https://github.com/tarsana/syntax)

- [X] Should parse and dump basic types: Boolean, Number, Array and Object.
- [X] Should define syntaxes using just a string.
- [X] Should define custom syntaxes easily.


### [Terminal](https://github.com/tarsana/terminal)

- [ ] Should write to console with formating and colors.
- [ ] Should read inputs from the console: character, key, word, line.
- [ ] Should handle interactive console.
- [ ] Should mock interactive console (useful for testing).


### [Command](https://github.com/tarsana/command)
A command should be able to:

- [X] Read from and write to console.
- [X] Easily define and parse command line args.
- [X] Show detailed help message.
- [X] Call another command and pass raw or parsed arguments.
- [X] Should be able to test any command.
- [ ] Compose other commands (pipe, parallel, switch, ...).
- [ ] Be lazy (writing changes to Filesystem only if everything goes well).
- [ ] Auto complete command line args.

### [Functional](https://github.com/tarsana/functional)

- [X] Should define useful functions (inspired from RamdaJS).
- [X] Should have a flexible and Lazy Stream class.
- [X] Should be as efficient as possible (sacrifice clean code).

# The Tarsana Command

...
