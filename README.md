# CIS1200 Dev Container

This is a [Visual Studio Code](https://code.visualstudio.com/) dev container for CIS1200.

## Getting Started
- Install [Docker](https://www.docker.com/products/docker-desktop)
- Install [Visual Studio Code](https://code.visualstudio.com/)
- Install the [Remote Development Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) for Visual Studio Code
- Clone this repository
- Open the repository in Visual Studio Code
- Click the remote button in the bottom left corner of Visual Studio Code and select "Reopen in Container"

## Using the Container

> Note: The Dockerfile under `.devcontainer/Dockerfile` is *not* used in the dev container environment. It will use a prebuilt image under the name `esinx/cis1200` which is build from the same Dockerfile.

This container is based on alpine linux and contains the following packages:

- Base OCaml packages (`ocamlbuild`, `merlin`, `ocaml-lsp-server`, etc.)
- utop
- camelot(1.7.1)

You may have to manually switch into `cis120`.

This project's Dockerfile is based off of the [OCaml Dockerfile](https://github.com/upenn-cis1xx/cis120-docker) from the original CIS1200 docker repository.

## Benefits

- Easy to set up and use
- Consistent environment for all TA/students
- VSCode support and syntax highlighting
- Inline camelot linting

## License

MIT

