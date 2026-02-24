# kami-markdown-to-html

[![KAMI Plugin](https://img.shields.io/badge/KAMI-plugin-8A2BE2)](https://github.com/Hypijump31/KAMI)
[![Signed](https://img.shields.io/badge/Ed25519-signed-green)](https://github.com/Hypijump31/kami-registry)

Convert Markdown to HTML with optional GFM extensions (tables, strikethrough, task lists).

## Install

```bash
kami install Hypijump31/kami-markdown-to-html@v0.1.0
```

## Usage

```bash
# Basic conversion
kami exec dev.kami.markdown-to-html '{"markdown": "# Hello\n\nThis is **bold** and *italic*."}'

# With GFM tables
kami exec dev.kami.markdown-to-html '{"markdown": "| A | B |\n|---|---|\n| 1 | 2 |"}'

# Disable specific extensions
kami exec dev.kami.markdown-to-html '{"markdown": "~~strike~~", "options": {"strikethrough": false}}'
```

## Arguments

| Name | Type | Required | Description |
|------|------|----------|-------------|
| `markdown` | string | yes | Markdown source text to convert |
| `options` | object | no | GFM options (all default to true) |

### Options

| Option | Type | Default | Description |
|--------|------|---------|-------------|
| `tables` | boolean | true | Enable GFM tables |
| `strikethrough` | boolean | true | Enable ~~strikethrough~~ |
| `tasklists` | boolean | true | Enable task lists |
| `smart_punctuation` | boolean | true | Convert quotes and dashes |

## Build from source

```bash
git clone https://github.com/Hypijump31/kami-markdown-to-html
cd kami-markdown-to-html
kami build . --release
```

To also package as plugin.zip:

```bash
kami build . --release --package
```

## Security

- Filesystem: none
- Network: none
- Max memory: 32 MB
- Max execution: 2000 ms

## License

MIT
