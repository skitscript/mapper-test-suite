# Skitscript Mapper Test Suite [![Continuous Integration](https://github.com/skitscript/mapper-test-suite/workflows/Continuous%20Integration/badge.svg)](https://github.com/skitscript/mapper-test-suite/actions) [![License](https://img.shields.io/github/license/skitscript/mapper-test-suite.svg)](https://github.com/skitscript/mapper-test-suite/blob/master/license) [![Renovate enabled](https://img.shields.io/badge/renovate-enabled-brightgreen.svg)](https://renovatebot.com/)

A test suite for mappers of Skitscript documents.

## Installation

It is recommended to install this as a Git submodule and use the included test
cases in your project's test suite:

```bash
git submodule add https://github.com/skitscript/mapper-test-suite submodules/skitscript/mapper-test-suite
```

### Renovate Updates

If you are using Renovate in your project, add
[the following](https://docs.renovatebot.com/modules/manager/git-submodules/) to
its `renovate.json` to automatically raise PRs when changes are pushed to this
repository:

```json
{
  "git-submodules": {
    "enabled": true
  }
}
```

## Usage

The [cases](./cases) directory contains a number of subdirectories.  Each
contains a standard set of files:

### [input.skitscript](./cases/four-decisions/input.skitscript)

This is the Skitscript file which is to be fed into the parser, then the mapper
during the test case.

### [output.json](./cases/four-decisions/output.json)

This is a JSON representation of the map which is expected to be produced in
response.

It is similar in structure to
[ValidMap](https://github.com/skitscript/types-nodejs/blob/master/ValidMap/index.ts).
