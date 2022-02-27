# action-mdbook-full

Install [mdbook](https://github.com/rust-lang/mdBook) with plugins enabled.

Plugins included:

Preprocessors:
- [mdbook-svgbob](https://github.com/drmingdrmer/mdbook-svgbob): SvgBob mdbook preprocessor which swaps code-blocks with neat SVG.
- [mdbook-katex](https://github.com/drmingdrmer/mdbook-katex): A preprocessor for mdBook, rendering LaTex equations to HTML at build time.

Backends:
- [mdbook-linkcheck](https://github.com/drmingdrmer/mdbook-linkcheck): A backend for `mdbook` which will check your links for you.


**This action only runs on `ubuntu-latest`**.


# Usage

```yaml
name: md book
on: [push]
jobs:
  mdbook:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v2
    - uses: drmingdrmer/mdbook-full@main
    - run: mdbook build
```
