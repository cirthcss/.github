# Cirth organization defaults

This repository powers the public profile and shared GitHub configuration for
the [Cirth organization](https://github.com/cirthcss).

It contains:

- the organization profile in [`profile/README.md`](profile/README.md);
- default community health files inherited by repositories that do not define
  their own;
- issue and pull request templates for future repositories;
- reusable and starter GitHub Actions workflows.

Repository-specific files always take precedence over these defaults.

## Shared workflows

The reusable Node CI workflow can be called from another repository:

```yaml
jobs:
  ci:
    uses: cirthcss/.github/.github/workflows/node-ci.yml@main
```

Consumers can override the Node version and working directory when needed.
See [`.github/workflows/node-ci.yml`](.github/workflows/node-ci.yml) for the
available inputs.
