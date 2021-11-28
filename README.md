# minimal-bulma

Personal blog theme powered by [Hugo](https://gohugo.io).

Heavily modified version of [minimal](https://github.com/calintat/minimal)
to use [bulma](https://bulma.io) and be more, well, minimal (fewer
dependencies, simplified formatting).

## Installation

You can install the theme either as a clone or submodule.

I recommend cloning and avoiding submodules like the plague... If you must
use submodules, type the following from the root of your Hugo site:

```
$ git submodule add https://github.com/deadlysyn/minimal-bulma.git themes/minimal-bulma
$ git submodule init
$ git submodule update
```

Now you can get updates by updating the submodule:

```
$ git submodule update --remote themes/minimal-bulma
```

## Configuration

After installation, take a look at the `exampleSite` folder inside `themes/minimal-bulma`.

To get started, copy the `config.toml` file inside `exampleSite` to the root of your Hugo site:

```
$ cp themes/minimal-bulma/exampleSite/config.toml .
```

Now edit this file and add your own information. Note that some fields can be omitted.

I recommend you use the theme's archetypes so now delete your site's `archetypes/default.md`.

## Features

You can tweak the look of the theme to suit your needs in a number of ways:

- The accent colour can be changed by using the `accent` field in `config.toml`.
- You can also change the background colour by using `backgroundColor`.

### Fonts

The theme uses [Google Fonts](https://fonts.google.com) to load its font. To change the font:

```toml
[params]
    font = "Source Code Pro" # should match the name on Google Fonts!
```

### Syntax highlighting

The theme supports syntax highlighting thanks to [highlight.js](https://highlightjs.org).

It's enabled by default, to disable set `highlight` to `false` in config.toml.

You can change the style used for the highlighting by using the `highlightStyle` field.

Only the "common" languages will be loaded by default. To load more, use `highlightLanguages`.

A list of all the available styles and languages can be found [here](https://highlightjs.org/static/demo/).

Please note the style and languages should be written in hyphen-separated lowercase, for example:

```toml
[params]
    highlight = true
    highlightStyle = "base16/gruvbox-dark-medium"
    highlightLanguages = ["bash", "c", "css", "go", "html", "json", "lua", "yaml"]
```
