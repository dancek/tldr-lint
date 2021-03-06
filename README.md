# tldr-lint

[![npm version][npm-image]][npm-url]
[![Build Status][github-actions-image]][github-actions-url]
[![David DM Dependency Status][dep-image]][dep-url]
[![Gitter chat][gitter-image]][gitter-url]

`tldr-lint` is a linting tool for validating [tldr](https://github.com/tldr-pages/tldr) pages.
It can also format your pages for you!


## Usage

It's really simple.

```
Usage: tldr-lint [options] <file|dir>

Options:
  -V, --version        output the version number
  -f, --format         also attempt formatting (to stdout, or as specified by -o)
  -o, --output <file>  output to formatted file
  -i, --in-place       formats in place
  -v, --verbose        print verbose output
  -h, --help           output usage information
```


## Linter errors

All of the errors can be found in [`lib/tldr-lint.js`](./lib/tldr-lint.js).

Error Code  | Description
:---------- | :-----------
TLDR001     | File should contain no leading whitespace
TLDR002     | A single space should precede a sentence
TLDR003     | Descriptions should start with a capital letter
TLDR004     | Command descriptions should end in a period
TLDR005     | Example descriptions should end in a colon with no trailing characters
TLDR006     | Command name and description should be separated by an empty line
TLDR007     | Example descriptions should be surrounded by empty lines
TLDR008     | File should contain no trailing whitespace
TLDR009     | Page should contain a newline at end of file
TLDR010     | Only Unix-style line endings allowed
TLDR011     | Page never contains more than a single empty line
TLDR012     | Page should contain no tabs
TLDR013     | Title should be alphanumeric with dashes, underscores or spaces
TLDR014     | Page should contain no trailing whitespace
TLDR015     | Example descriptions should start with a capital letter
TLDR101     | Command description probably not properly annotated
TLDR102     | Example description probably not properly annotated
TLDR103     | Command example is missing its closing backtick
TLDR104     | Example descriptions should prefer infinitive tense (e.g. write) over present (e.g. writes) or gerund (e.g. writing)
TLDR105     | There should be only one command per example
TLDR106     | Page title should start with a hash (`#`)

## To-do

- Assert file has .md extension
- Assert file name is same as page title

[npm-url]: https://www.npmjs.com/package/tldr-lint
[npm-image]: https://img.shields.io/npm/v/tldr-lint.svg

[github-actions-url]: https://github.com/tldr-pages/tldr-lint/actions
[github-actions-image]: https://img.shields.io/github/workflow/status/tldr-pages/tldr-lint/Tests/master.svg

[dep-url]: https://david-dm.org/tldr-pages/tldr-lint
[dep-image]: https://david-dm.org/tldr-pages/tldr-lint.svg?theme=shields.io

[dev-dep-url]: https://david-dm.org/tldr-pages/tldr-lint#info=devDependencies
[dev-dep-image]: https://david-dm.org/tldr-pages/tldr-lint/dev-status.svg?theme=shields.io

[gitter-url]: https://gitter.im/tldr-pages/tldr
[gitter-image]: https://badges.gitter.im/tldr-pages/tldr.png
