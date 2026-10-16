# roman-mendoza.github.io

Documentation site built with [Zensical](https://zensical.org/), published at
<https://roman-mendoza.github.io/>.

## Local development

Use Python 3.12 and create a virtual environment:

```sh
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
zensical serve
```

Open <http://localhost:8000/> to preview the site. On Windows, activate the
environment with `.venv\Scripts\activate` instead.

Edit Markdown files in `docs/` and update `nav` in `zensical.toml` when adding
pages.

## Build

```sh
zensical build --clean --strict
```

The generated site is written to `site/`, which is ignored by Git.

## Deployment

In the repository's **Settings → Pages**, select **GitHub Actions** as the
build and deployment source. The Documentation workflow builds pull requests
and deploys pushes to `main`. It can also be run manually on `main`.
