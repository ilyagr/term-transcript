# term-transcript CLI

This crate provides command-line interface for `term-transcript`. It allows capturing
terminal output to SVG and testing the captured snapshots.

## Usage

- The `capture` subcommand captures output from stdin, renders it to SVG and
  outputs SVG to stdout.
- The `exec` subcommand executes one or more commands in the shell, captures
  their outputs, renders to an SVG image and outputs it to stdout.
- The `test` subcommand allows testing snapshots from the command line.

Launch the CLI with the `--help` option for more details about arguments
for each subcommand.

### Examples

This example creates [a snapshot](../tests/snapshots/rainbow.svg)
of [the `rainbow` example](../examples/rainbow.rs) and then tests it.

![Testing rainbow example](tests/snapshots/test.svg)

The snapshot itself [is tested](tests/e2e.rs), too! It also shows
that SVG output by the program is editable; in the snapshot, this is used to
highlight command-line args and to change color of comments in the user inputs.

## License

Licensed under either of [Apache License, Version 2.0](LICENSE-APACHE)
or [MIT license](LICENSE-MIT) at your option.

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in `term-transcript` by you, as defined in the Apache-2.0 license,
shall be dual licensed as above, without any additional terms or conditions. 