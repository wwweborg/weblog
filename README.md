# Weblog

A minimalist Hugo theme for a developer's personal journal.
Floating capsule header, automatic light/dark mode, self-hosted
fonts and a subtle noise background.

![Screenshot](https://raw.githubusercontent.com/TUUSUARIO/weblog/main/images/screenshot.png)

[Live demo](https://tu-demo.example) · [Report an issue](https://github.com/TUUSUARIO/weblog/issues)

## Features

- Light and dark mode that follows the system setting
- Floating capsule header with avatar, handle, section icons and social links
- Narrow reading column and a journal-style post list
- Self-hosted fonts (Golos Text and Roboto Mono), no third-party requests
- Swappable SVG icons

## Requirements

Hugo 0.146.0 or later.

## Installation

### As a Hugo Module

```bash
hugo mod init github.com/you/your-site
```

```toml
[module]
  [[module.imports]]
    path = 'github.com/TUUSUARIO/weblog'
```

### As a Git submodule

```bash
git submodule add https://github.com/TUUSUARIO/weblog themes/weblog
```

```toml
theme = 'weblog'
```

## Configuration

```toml
[params]
  handle = '@yourname'
  avatar = 'avatar.jpg'        # place the image in static/

[menus]
  [[menus.main]]
    name = 'Home'
    pageRef = '/'
    weight = 10
    [menus.main.params]
      icon = 'home'

  [[menus.social]]
    name = 'GitHub'
    url = 'https://github.com/yourname'
    weight = 10
    [menus.social.params]
      icon = 'github'
```

`pageRef` must point to pages that exist in your site.

## Icons

Each `icon` value is the name of a file in `assets/icons/`
(for example `github` → `assets/icons/github.svg`). To add one, drop
an SVG into your site's `assets/icons/` folder.

## Credits

- [Golos Text](https://fonts.google.com/specimen/Golos+Text) and
  [Roboto Mono](https://fonts.google.com/specimen/Roboto+Mono), SIL Open Font License 1.1
- [Meteor Icons](https://github.com/meteor-icons/meteor-icons), MIT License

## License

MIT