# Changelog

All notable changes to this project will be documented in this file.
The project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

- Support interacting with shell using pseudo-terminal (PTY) via `portable-pty`
  crate.

### Changed

- Update `handlebars` and `pretty_assertions` dependencies.
- Generalize `TermError::NonCsiSequence` variant to `UnrecognizedSequence`.

### Fixed

- Fix flaky PowerShell initialization that could lead to the init command
  being included into the captured output.
- Fix parsing of `90..=97` and `100..=107` SGR params (i.e., intense foreground
  and background colors).
- Enable parsing OSC escape sequences; they are now ignored instead of leading
  to a `TermError`.
- Process carriage return `\r` in terminal output. (As a stopgap measure, the text
  before `\r` is not rendered.)
- Fix rendering intense colors into HTML. Previously, intense color marker
  was dropped in certain cases.
- Fix waiting for echoed initialization commands.
- Add `height` attribute to top-level SVG to fix its rendering.

## 0.1.0 - 2021-06-01

The initial release of `term-transcript`.