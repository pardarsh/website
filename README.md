# Pardarsh website

The project site for **Pardarsh**: open infrastructure for public records that
are traceable, attributable and machine-readable.

It introduces the two projects and collects the writing behind them:

- [pardarsh-core](https://github.com/pardarsh/pardarsh-core): application-agnostic
  Rust infrastructure for public records (stable IDs, attributable history,
  provenance, typed relationships, verifiable export).
- **Loklekha**: the civic ledger app built on pardarsh-core.

## Structure

```
index.html      the whole site (one page)
style.css       styles, including dark mode
.github/        CI, Pages deploy, issue and PR templates
```

Plain HTML and CSS. No build step, no JavaScript, no dependencies.

## Run locally

Open `index.html` in a browser, or serve the folder:

```sh
python -m http.server 8000
# then visit http://localhost:8000
```

## Add an article, thesis or doc

In `index.html`, find the `Writing & docs` section and copy one
`<li class="entry">` block. Set `data-kind` to `essay`, `thesis`, `doc` or
`talk` (it only changes the label colour), then edit the link, title and
one-line summary.

## Checks

Install [pre-commit](https://pre-commit.com) once, then enable the hooks:

```sh
pip install pre-commit
pre-commit install
pre-commit run --all-files
```

CI runs the same hooks, validates the HTML with
[html-validate](https://html-validate.org), and checks links with
[lychee](https://github.com/lycheeverse/lychee).

## Deploy

Pushing to `main` publishes the site to GitHub Pages through
`.github/workflows/pages.yml`. In the repository settings, set
**Pages → Source** to **GitHub Actions** once.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md), [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)
and [SECURITY.md](SECURITY.md).
