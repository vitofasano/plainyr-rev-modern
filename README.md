# plainyr-rev-modern (v0.2.4)

A modernized version of the `plainyr` BibTeX style, featuring **reverse chronological ordering** (newest to oldest) and enhanced DOI support.

## Key Features
* **Reverse Chronological Order**: Automatically sorts your bibliography starting from the most recent year.
* **Robust DOI Support**: Perfect handling of special characters (like underscores `_`) in DOI strings.
* **Clickable Links**: Generates active links via the `https://doi.org/` resolver.
* **URL Field Support**: Full support for the url field across all standard entry types.
* **Global Toggles**: Easily enable or disable features (like URLs) by editing a single line in the .bst file.

## ⚠️ Mandatory Requirement
To ensure DOIs and underscores are rendered correctly, you **must** include the `hyperref` package in your LaTeX preamble:

```latex
\usepackage{hyperref}
```

## Usage
1. Download `plainyr-rev-modern.bst` and place it in your project folder.
2. In your `.tex` file, set the style:

```latex
\bibliographystyle{plainyr-rev-modern}
\bibliography{your-bib-file}
```
## Customization
Bibliography behavior can be customized by editing the setup.options function located near the end of the plainyr-rev-modern.bst file (following the READ command):

```bst
FUNCTION {setup.options}
{ 
  #1 'show.url :=   % Set to 1 to show URLs, 0 to hide them
}
```

## Contributing
Feel free to open issues or pull requests to improve this style!

## License
This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

## Roadmap
- [x] Rename project to `plainyr-rev-modern` (v0.2.3)
- [x] Add reverse chronological sorting by default
- [x] Improved DOI support with underscore handling
- [x] Added `examples/` folder with test suite
- [x] Add `URL` field support (v0.2.4)
- [ ] Add optional `abstract` field display
- [ ] Implement author name cleaning/abbreviation (e.g., "V. Fasano")
- [ ] Add toggle for normal vs. reverse chronological sorting
- [ ] Final rebranding to `plainyr-modern`
