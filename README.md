# Pre-commit git hooks

Git hooks to integrate with [pre-commit](http://pre-commit.com).


<!--TOC-->

- [Configure pre-commit](#configure-pre-commit)
- [Two ways to invoke pre-commit](#two-ways-to-invoke-pre-commit)
- [Available hooks](#available-hooks)
  - [`check-ruby-debug`](#check-ruby-debug)
- [Contributing](#contributing)
- [Testing](#testing)
- [License](#license)

<!--TOC-->


## Configure pre-commit

:warning: These hooks now require Python3.

Add to `.pre-commit-config.yaml` in your git repo:

    - repo: https://github.com/jumanjihouse/pre-commit-hooks
      rev: master  # or specific git tag
      hooks:
        - id: check-ruby-debug

## Two ways to invoke pre-commit

If you want to invoke the checks as a git pre-commit hook, run:

    pre-commit install

If you want to run the checks on-demand (outside of git hooks), run:

    pre-commit run --all-files --verbose



## Available hooks

### `check-ruby-debug`

**What it does**

* Check if any file with `.rb` or `.erb` extentions contain `byebug`, `binding.b` or `binding.break`

## Contributing

Please see [CONTRIBUTING.md](CONTRIBUTING.md).


## License

The code in this repo is licensed under the [MIT License](LICENSE).
