# Golangci-lint Golden Config

Opinionated [golangci-lint](https://github.com/golangci/golangci-lint) configuration. Intentionally strict (but not draconian) to surface bugs, security issues, and style problems early while avoiding the noisiest checks.

> It was originally published as a popular [github gist](https://gist.github.com/maratori/47a4d00457a92aa426dbd48a18776322) ![Stars](https://img.shields.io/github/gist/stars/47a4d00457a92aa426dbd48a18776322?label=stars&style=flat-square)

## Quick Start

1. Copy `.golangci.yml` to the root of your Go module.
2. Set `formatters.settings.goimports.local-prefixes` to your module path (for example, `github.com/acme/service`).
3. Run `golangci-lint run ./...` from the project root.

## Versioning

- Tags mirror the matching [golangci-lint releases](https://github.com/golangci/golangci-lint/releases); a few versions may be missing.
- This keeps it friendly to automation tools such as [updatecli](https://updatecli.io).

## Customizing

- Adjust the module prefix (`formatters.settings.goimports.local-prefixes`).
- Toggle linters or tune their settings to match your risk tolerance.
- Refine `linters.exclusions.rules`.
- Optional extras are marked with `## you may want to enable`; uncomment what you need.

## What's Inside

- Every supported linter and formatter is listed, with disabled ones commented for quick discovery.
- Each entry includes a short comment explaining its purpose.
- Only non-default options appear here; full defaults live in [.golangci.reference.yml](https://github.com/golangci/golangci-lint/blob/main/.golangci.reference.yml).
- Common false positives are pre-collected under `linters.exclusions.rules`.

## License

MIT License. See [LICENSE](/LICENSE) for details.
