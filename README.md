# About

A [Devbox](https://www.jetify.com/docs/devbox/) plugin to set up a project-specific global directory for node.js package managers.

This solves the issue of installing global packages described in the [Installing Global Packages](https://www.jetify.com/docs/devbox/devbox_examples/languages/nodejs/#installing-global-packages) section.

Supports npm, pnpm

# Installation
Add `nodejs` as a dependency and then add the plugin to the `include` section in your `devbox.json` file:
```
"packages": [
    "nodejs"
],
"include": [
    "github:martingreber/nodejs-global-devbox-plugin"
]
```
Example [devbox.json](test/devbox.json)

# Usage
Example of installing tailwindcss with npm:
```shell
$ devbox shell
$ npm install -g tailwindcss @tailwindcss/cli
$ tailwindcss
≈ tailwindcss v4.0.14

Usage:
  tailwindcss [--input input.css] [--output output.css] [--watch] [options…]
  ...
$ exit
$ tailwindcss
command not found: tailwindcss
```