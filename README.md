# SML Syntax for VSCode (NoCode)

VSCode syntax extension for **SML (Simple Markup Language)** used by NoCodeGodot (`SMLCore` / `NoCodeRunner`).

## Features

- Language registration for `.sml`
- Syntax highlighting for:
  - SML node names (`Window`, `Column`, `Panel`, ...)
  - property keys (`text:`, `layoutMode:`, ...)
  - strings, escapes, booleans, integers
  - enum-like values used by runtime schema (e.g. `layout`, `fixed`, `document`, `open`, `saveAs`)
  - comments (`//`, `/* ... */`)

No language server is required.

## Example

```qml
Window {
  title: "NoCode"
  width: 1024
  height: 768
  scaling: fixed
  layoutMode: app

  Column {
    spacing: 8
    Label {
      text: "Hello SML"
    }
  }
}
```

## Local test release (.vsix)

Prerequisites:

- Node.js + npm
- VSCode CLI (`code` in PATH)

Install dependencies:

```bash
npm install
```

Build VSIX:

```bash
npm run package
```

Install latest VSIX locally:

```bash
npm run install-local
```

## Publish scripts

### Visual Studio Marketplace

Set token:

```bash
export VSCE_PAT="<your-marketplace-token>"
```

Publish:

```bash
npm run publish:marketplace
```

### Open VSX

Set token:

```bash
export OVSX_PAT="<your-openvsx-token>"
```

Publish:

```bash
npm run publish:openvsx
```

## Part of NoCode ecosystem

See: [NoCodeGodot](https://github.com/CrowdWare/NoCodeGodot)