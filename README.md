# Nix flake templates for easy dev environments

[![built with nix](https://builtwithnix.org/badge.svg)](https://builtwithnix.org)

To initialize (where `${ENV}` is listed in the table below):

```shell
nix flake init --template "https://flakehub.com/f/the-nix-way/dev-templates/*#${ENV}"
```

Here's an example (for the [`rust`](./rust) template):

```shell
# Initialize in the current project
nix flake init --template "https://flakehub.com/f/the-nix-way/dev-templates/*#rust"

# Create a new project
nix flake new --template "https://flakehub.com/f/the-nix-way/dev-templates/*#rust" ${NEW_PROJECT_DIRECTORY}
```

## How to use the templates

Once your preferred template has been initialized, you can use the provided shell in two ways:

1. If you have [`nix-direnv`][nix-direnv] installed, you can initialize the environment by running `direnv allow`.
2. If you don't have `nix-direnv` installed, you can run `nix develop` to open up the Nix-defined shell.

## Available templates

| Environment | Template            |
| :---------- | :------------------ |
| [crypto]    | [`crypt`](./crypt/) |
