# Docco (with Kotlin Support)

```
 ____
/\  _`\
\ \ \/\ \        ___         ___         ___         ___
 \ \ \ \ \      / __`\      /'___\      /'___\      / __`\
  \ \ \_\ \    /\ \ \ \    /\ \__/     /\ \__/     /\ \ \ \
   \ \____/    \ \____/    \ \____\    \ \____\    \ \____/
    \/___/      \/___/      \/____/     \/____/     \/___/
```

This is a fork of [jashkenas/docco](https://github.com/jashkenas/docco) with **Kotlin language support** added.

## What's New in This Fork

### ✨ Kotlin Language Support

This fork adds support for **Kotlin** (`.kt` files) to Docco's language definitions.

- **File extension**: `.kt`
- **Comment style**: `//` (single-line comments, same as Java/JavaScript/C++)
- **Syntax highlighting**: Uses Highlight.js's built-in Kotlin support

### Changes Made

- Added Kotlin entry to `resources/languages.json`:
  ```json
  ".kt": {"name": "kotlin", "symbol": "//"}
  ```

This enables Docco to generate beautiful literate programming documentation for Kotlin source code, just like it does for Java, JavaScript, Python, and other supported languages.

## Original Docco Information

Docco is a quick-and-dirty, hundred-line-long, literate-programming-style documentation generator.

For more information about the original project, see: http://ashkenas.com/docco/

## Installation

### Install from npm (once published)

```bash
npm install -g @ackshaey/docco-kotlin
```

### Install from source

```bash
git clone https://github.com/ackshaey/docco.git
cd docco
npm install
npm link
```

## Usage

```bash
docco [options] FILES
```

### Options

- `-h, --help` - Output usage information
- `-V, --version` - Output the version number
- `-l, --layout [layout]` - Choose a built-in layout (parallel, linear)
- `-c, --css [file]` - Use a custom CSS file
- `-o, --output [path]` - Use a custom output path
- `-t, --template [file]` - Use a custom .jst template
- `-e, --extension [ext]` - Use the given file extension for all inputs
- `-L, --languages [file]` - Use a custom languages.json
- `-m, --marked [file]` - Use custom marked options

### Kotlin Example

```bash
# Generate documentation for Kotlin files
docco src/**/*.kt

# With custom output directory
docco -o docs src/**/*.kt
```

## Supported Languages

This fork supports all the original Docco languages plus:

- **Kotlin** (`.kt`) - NEW!
- JavaScript, CoffeeScript, Ruby, Python
- Java, Scala, C, C++, C#
- And many more...

For the complete list, see [resources/languages.json](resources/languages.json).

## Why This Fork?

The original Docco project doesn't currently support Kotlin. This fork was created to enable documentation generation for Kotlin codebases, particularly for projects like [Firecode.io](https://firecode.io) that use Kotlin for their problem sets and need to generate annotated solution documentation.

## Contributing to Upstream

If you'd like to see Kotlin support in the official Docco project, please consider:

1. Opening an issue at [jashkenas/docco](https://github.com/jashkenas/docco/issues)
2. Submitting a pull request with these changes

## License

This project maintains the same license as the original Docco project.

See [LICENSE](LICENSE) for details.

## Credits

- **Original Docco**: Created by [Jeremy Ashkenas](https://github.com/jashkenas)
- **Kotlin Support**: Added by [Ackshaey Singh](https://github.com/ackshaey)

---

## Links

- **Original Docco Repository**: https://github.com/jashkenas/docco
- **This Fork**: https://github.com/ackshaey/docco
- **Highlight.js** (provides syntax highlighting): https://highlightjs.org/
- **Marked** (Markdown parser): https://marked.js.org/
