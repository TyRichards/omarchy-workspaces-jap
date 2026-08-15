# Omarchy Workspaces (JAP)

A Quickshell bar widget for Omarchy Quattro that displays workspace numbers as Japanese numerals.

Workspaces 1–10 are rendered as `一 二 三 四 五 六 七 八 九 十`. Occupied and focused workspace behavior follows Omarchy's native Workspaces widget.

## Requirements

- Omarchy Quattro
- No external dependencies or privileged setup

## Install

Disable the native Workspaces widget, then install and enable this replacement:

```sh
omarchy plugin disable omarchy.workspaces
omarchy plugin add https://github.com/TyRichards/omarchy-workspaces-jap.git --enable
```

If needed, place it in the left section:

```sh
omarchy bar move io.github.tyrichards.workspaces-jap --section left
```

## Usage

Click a Japanese workspace numeral to focus that workspace.

## Validate

```sh
omarchy plugin validate ~/.config/omarchy/plugins/io.github.tyrichards.workspaces-jap
qmllint -I "$OMARCHY_PATH/shell" \
  ~/.config/omarchy/plugins/io.github.tyrichards.workspaces-jap/Workspaces.qml
```

## Remove

Remove the plugin and restore Omarchy's native Workspaces widget:

```sh
omarchy plugin remove io.github.tyrichards.workspaces-jap --yes
omarchy plugin enable omarchy.workspaces left
```

## License

MIT. This plugin is derived from Omarchy's native Workspaces widget.
