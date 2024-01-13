FROM mcr.microsoft.com/devcontainers/base:alpine

RUN apk update \
    && apk add --no-cache --update m4 opam bubblewrap make gcc g++ python3 py3-pip git bash git pkgconfig libx11-dev ncurses

USER vscode
RUN opam init --disable-sandboxing -a --shell=bash
RUN opam switch create cis120 ocaml-base-compiler.4.12.0

RUN opam install -y \
    camelot.1.7.1 \
    ocamlbuild \
    ocamlfind \
    yojson \
    merlin \
    js_of_ocaml \
    js_of_ocaml-lwt \
    ocp-indent \
    utop \
    graphics \
    dune \
    odoc \
    ppx_expect \
    ocaml-lsp-server.1.8.0 \
    ocamlformat.0.26.1 

RUN opam clean
RUN echo 'eval $(opam env)' >> ~/.bashrc