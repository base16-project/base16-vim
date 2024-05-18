# Contributing

This repository includes a [GitHub Action] that builds the
colorschemes once a week. This keeps the colorschemes up-to-date
automatically.

## Building

### Dependencies

- `>=0.2.6` [base16-builder-go]

### Usage for template editing

1. Clone the template repository onto your system
2. Download the [latest base16-builder-go binary]
3. Execute the binary with the `-template-dir` arg and provide
   `/path/to/base16-vim` 

Or the above steps represented in shell commands:

```shell 
/path/to/base16-builder-go-binary \
  -template-dir "/path/to/base16-vim"
```

### Usage for adding or editing a colorscheme

1. Clone the base16-vim
2. Clone [schemes]
3. Download the [latest base16-builder-go binary]
4. Execute the binary with 
  - `-schemes-dir` arg - provide `/path/to/schemes/base16`
  - `-template-dir` arg - provide `/path/to/base16-vim`
    (`base16-vim` repository)

```shell
/path/to/base16-builder-go-binary \
  -schemes-dir "/path/to/schemes/base16" \
  -template-dir "/path/to/base16-vim"
```

If you have more questions about [base16-builder-go], have a look at
the information on the GitHub page.

## Submitting a PR

- Run the colorscheme generation using [base16-builder-go] and commit
  the changes in your PR. Don't make changes directly to the generated
  colorschemes, make changes to the template instead.
- Please abide by what's requested in the [PR template].

## Submitting an issue

Please follow the instructions in the issue templates:

- [Issue template for bug reports]
- [Issue template for feature requests]

[base16-builder-go]: https://github.com/tinted-theming/base16-builder-go
[schemes]: https://github.com/tinted-theming/schemes
[GitHub Action]: .github/workflows/update.yml
[latest base16-builder-go binary]: https://github.com/tinted-theming/base16-builder-go/releases
[PR template]: .github/pull_request_template.md
[Issue template for bug reports]: .github/ISSUE_TEMPLATE/bug_report.md
[Issue template for feature requests]: .github/ISSUE_TEMPLATE/feature_request.md
