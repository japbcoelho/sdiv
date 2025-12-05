# Changelog

All notable changes to the sdiv package will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

## [1.0.0] - 2025-12-05

### Added
- Initial release
- `\sdiv` command for drawing successive division diagrams
- Support for `circle`/`highlight` option to highlight remainders with default inner sep of 0.25
- Support for `uline` option to underline remainders and final quotient using the ulem package
- Support for `arrow` option to show reading direction
- Custom inner sep parameter for adjustable circle sizes
- Automatic layout with dynamic spacing
- Input validation for dividend and divisor
- Proper alignment of numbers in columns
- Support for large numbers
- English error messages
- Ability to combine options (circle, uline, arrow)

### Features
- Works with LuaLaTeX
- Uses TikZ for graphics
- Uses ulem package for underlining
- Clean, professional output
- Flexible options system
- Fixed gap between numbers and vertical bars

### Known Issues
- Very large inner sep values (> 2) may cause circle overlap with bars
  - Recommendation: use moderate values (< 1.0)
