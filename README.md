# sdiv

[![License: LPPL v1.3c](https://img.shields.io/badge/License-LPPL%20v1.3c-blue.svg)](https://www.latex-project.org/lppl.txt)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](https://github.com/japbcoelho/sdiv)

A LaTeX package for drawing successive division diagrams (commonly used for base conversion).

## Description

The `sdiv` package provides the `\sdiv` command to typeset successive division diagrams in a clean, customizable format. These diagrams are particularly useful for:

- Converting numbers between bases
- Teaching division algorithms
- Visualizing iterative division processes

## Features

- Clean, professional-looking diagrams
- Customizable circle sizes (inner sep)
- **Underline option** for highlighting remainders and quotients
- Optional arrow indicating reading direction
- Automatic layout and spacing
- Support for large numbers
- Proper alignment of all elements

## Installation

### From GitHub (Development Version)

```bash
# Clone the repository
git clone https://github.com/japbcoelho/sdiv.git
cd sdiv

# Copy to your local texmf tree
mkdir -p ~/texmf/tex/latex/sdiv
cp sdiv.sty ~/texmf/tex/latex/sdiv/
texhash ~/texmf
```

### Automatic Installation (via CTAN)

Once available on CTAN, install using your TeX distribution's package manager:

```bash
tlmgr install sdiv
```

### Manual Installation

1. Download `sdiv.sty` from the [releases page](https://github.com/japbcoelho/sdiv/releases)
2. Place it in your local `texmf` tree:
   - Linux/Mac: `~/texmf/tex/latex/sdiv/`
   - Windows: `C:\Users\<username>\texmf\tex\latex\sdiv\`
3. Run `texhash` or `mktexlsr`

Or simply place `sdiv.sty` in the same directory as your `.tex` file.

## Basic Usage

```latex
\documentclass{article}
\usepackage{sdiv}

\begin{document}
% Basic division: 97 ÷ 5
\[\sdiv{97}{5}\]

% With circles highlighting remainders
\[\sdiv[circle]{97}{5}\]

% With underlined remainders and quotient
\[\sdiv[uline]{97}{5}\]

% With arrow showing reading direction
\[\sdiv[arrow]{97}{5}\]

% Combine options
\[\sdiv[circle,arrow]{97}{5}\]
\[\sdiv[uline,arrow]{97}{5}\]

% Custom circle size (inner sep in em)
\[\sdiv[0.5,arrow]{255}{2}\]
\end{document}
```

## Syntax

```latex
\sdiv[options]{dividend}{divisor}
```

**Options:**
- `circle` or `highlight`: Draw circles around remainders and final quotient
- `uline`: Underline remainders and final quotient using the ulem package
- `arrow`: Draw an arrow indicating reading direction (for base conversion)
- `<number>`: Set custom circle inner sep (e.g., `0.5`, `1.0`)
  - Can be combined with other options (e.g., `0.3,arrow`, `uline,arrow`)

**Arguments:**
- `dividend`: Non-negative integer
- `divisor`: Positive integer (non-zero)

## Examples

See `example.tex` for comprehensive examples including:
- Simple divisions
- Base conversion (binary, octal, hexadecimal)
- Large numbers
- Custom circle sizes

## Requirements

- LuaLaTeX (required for Lua code execution)
- TikZ package (automatically loaded)

## Known Limitations

- **Requires LuaLaTeX**: This package uses Lua code and will not work with pdfLaTeX or XeLaTeX
- **Large inner sep overlap**: When using very large custom inner sep values (e.g., > 2), circles may overlap with vertical bars. This is a known issue that will be addressed in a future version. For now, use moderate values (< 1.0) for best results.

## Version History

See `CHANGELOG.md` for detailed version history.

## License

This work may be distributed and/or modified under the conditions of the LaTeX Project Public License, either version 1.3c of this license or (at your option) any later version.

The latest version of this license is in:
  http://www.latex-project.org/lppl.txt

This work has the LPPL maintenance status `maintained`.

## Author

**Joao Alberto Coelho**
Email: japbcoelho@proton.me

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

For bug reports and feature requests, please open an issue on GitHub.

## See Also

- Documentation: `sdiv.pdf`
- Example file: `example.tex`
