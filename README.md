# z

[![Build Status](https://travis-ci.org/cjp/z.svg?branch=master)](https://travis-ci.org/cjp/z)
[![Code Climate](https://codeclimate.com/github/cjp/z/badges/gpa.svg)](https://codeclimate.com/github/cjp/z)

`z` is an absurdly minimal static site generator written in Go.

It's a fork of the [zs] static site generator, which is in turn inspired
by the [zas] static site generator.

`z` is *even more* minimal.

The name is an obvious progression of minimalism.

## Features

* Zero configuration
* Cross-platform
* Fast

## Installation

Build it with go:

	$ go get github.com/cjp/z

## Ideology

* Content must be markdown.
* Layout templates must be [amber].
* Style sheets shall be [gcss].

Keep all service files (layout pages, deployment scripts etc)
in the `.z` subdirectory.

Define variables in the header of the content files using [YAML]:

    ---
    title: My web site
	keywords: best website, hello, world
	---

	Markdown text goes after a header *separator*

Variables are inserted using typical amber notation `#{title}`.

## Command line usage

`z build` re-builds your site.

`z build <file>` re-builds one file and prints resulting content to stdout.

`z watch` rebuilds your site every time you modify any file.

`z var <filename> [var1 var2...]` prints a list of variables defined in the
header of a given markdown file, or the values of certain variables (even if
it's an empty string).

## License

The software is distributed under the MIT license.

[amber]: https://github.com/eknkc/amber/
[YAML]: https://github.com/go-yaml/yaml
[gcss]: https://github.com/yosssi/gcss
[zs]: https://github.com/zserge/zs
[zas]: https://github.com/imdario/zas
