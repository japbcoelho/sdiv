# Contributing to sdiv

Thank you for considering contributing to the sdiv package! This document provides guidelines for contributing to the project.

## How to Contribute

### Reporting Bugs

If you find a bug, please open an issue on GitHub with:
- A clear, descriptive title
- Detailed steps to reproduce the issue
- Expected behavior vs. actual behavior
- Minimal example code that demonstrates the problem
- Your TeX distribution and version (e.g., TeX Live 2025)
- The version of sdiv you're using

### Suggesting Enhancements

Enhancement suggestions are welcome! Please open an issue with:
- A clear description of the enhancement
- Use cases and examples
- Why this enhancement would be useful

### Pull Requests

1. Fork the repository
2. Create a new branch for your feature (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Test your changes thoroughly with LuaLaTeX
5. Update documentation if needed
6. Commit your changes with clear, descriptive messages
7. Push to your branch (`git push origin feature/amazing-feature`)
8. Open a Pull Request

### Development Guidelines

- The package must remain compatible with LuaLaTeX
- All code should include clear comments
- Follow the existing code style
- Test with various inputs (edge cases, large numbers, etc.)
- Update `CHANGELOG.md` for significant changes
- Ensure all documentation is in English

## Testing

Before submitting a pull request, please test your changes:

```bash
# Compile the documentation
lualatex sdiv.tex

# Compile the examples
lualatex example.tex

# Test with your own examples
```

## Code of Conduct

- Be respectful and constructive
- Welcome newcomers and help them learn
- Focus on what is best for the community
- Show empathy towards other community members

## Questions?

If you have questions, feel free to open an issue or contact the maintainer at japbcoelho@proton.me

## License

By contributing to sdiv, you agree that your contributions will be licensed under the LPPL 1.3c license.
