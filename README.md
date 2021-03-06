# lin
lin is a stack-based language that aims to be as straightforward and simple as possible.

## Normal Installation

    npm i -g linlang

## Manual Installation
`git clone` this repo, `cd` into it, `npm install`, and `npm ln`.

## Language Specs
CLI Usage:

    lin program.lin

For more options, run `lin -h`.

To get an idea of the language syntax, see `examples/` and `docs/`.

### Program Execution
The parsing is extremely basic. The code is parsed line-by-line; numbers match the pattern `[0-9]*\.?[0-9]+|[0-9]+\.?`, keywords match the pattern `[^0-9. ]+`, and spaces are ignored. This means that a valid lin snippet is really just a series of numbers and keywords.

By default, only the first line is parsed and interpreted. It is possible to execute other lines through functions.

### Special Syntax
Any keyword with a `\` in front of it will push the rest of the keyword (excluding the leading `\`) onto the stack. Any keyword with `#` in front of it will be ignored or treated as an ID. Other than that, numbers get pushed to the stack, and keywords are executed as commands.

### Commands
See `docs/commands.md`. Concepts and terms in that file are explained in the other files of `docs/`.
