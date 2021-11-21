# Cartoview Documentation

This repository is used to edit and build Cartoview documentation available at [http://cartologic.github.io](http://cartologic.github.io/).

## Development

To run and edit this documentation locally, please follow the upcoming steps.

- Create [Python Virtual Environment](https://docs.python.org/3/tutorial/venv.html).

```shell
virutalenv -p python3 docs_venv
# Activate the virutal env
## Linux
source docs_venv/bin/activate
## Windows
.\docs_venv\Scripts\activate.bat
```

- Install [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/getting-started/#installation) using pip.

```shell
pip install mkdocs-material
```

- Run the documentation.

```shell
# Run on localhost:8000
mkdocs serve
# Run on different port (e.g. 7070)
mkdocs serve -a localhost:7070
```

- Each time you edit inside **docs** folder, the hard-reload will update accordingly.

## Build and Deploy

When you're finished editing, you can build a static site from your Markdown files.

```shell
mkdocs build
```

This will generate a folder called **site** that can be hosted on any web server.

Each time there's a pushed new commit, a new **site** is automatically built and deployed to [GitHub pages](https://pages.github.com/) (e.g. [cartologic.github.io](https://cartologic.github.io/)) using GitHub actions workflow (e.g. `.github/workflows/MkDocs-CI.yml`) to automate the build and deployment of the documentation.
