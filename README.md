# About

A [Devbox](https://www.jetify.com/docs/devbox/) plugin to set up a project-specific npm prefix directory.
This makes `npm install -g <package>` install global packages only to your current devbox shell. This solves the
issue described in the [Installing Global Packages](https://www.jetify.com/docs/devbox/devbox_examples/languages/nodejs/#installing-global-packages) section.

# Installation
Add the plugin to the `include` section in your `devbox.json` file:
```
"include": [
    "github:martingreber/nodejs-global-devbox-plugin"
]
```
Example [devbox.json](test/devbox.json)

# Usage
Example of installing tailwindcss:
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