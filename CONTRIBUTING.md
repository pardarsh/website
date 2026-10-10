# Contributing

Thanks for helping improve the Pardarsh website. This repository is only the
project site; code contributions to the infrastructure belong in
[pardarsh-core](https://github.com/pardarsh/pardarsh-core).

## Good first contributions

- Fixing typos, unclear wording or broken links.
- Adding an article, talk or doc to the **Writing & docs** section.
- Accessibility improvements (contrast, headings, keyboard navigation).

## How to contribute

1. Open an issue first for anything beyond a small fix, so we can agree on the
   change before you spend time on it.
2. Fork the repository and create a branch from `main`.
3. Make your change. Keep the site dependency-free: plain HTML and CSS, no
   build step, no tracking scripts.
4. Run the checks:
   ```sh
   pre-commit run --all-files
   npx html-validate index.html
   ```
5. Check the page in a browser at desktop and phone widths, in light and dark
   mode.
6. Open a pull request describing what changed and why.

## Style

- Keep copy short and plain. Avoid jargon where an everyday word works.
- Reuse the colour tokens defined at the top of `style.css`; do not hard-code
  new colours.
- External links open in a new tab with `rel="noopener"`.

By participating you agree to follow the [Code of Conduct](CODE_OF_CONDUCT.md).
