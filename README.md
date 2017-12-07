# Enabling Jupyter Extensions with post-build commands

[![Binder](https://beta.mybinder.org/badge.svg)](https://beta.mybinder.org/v2/gh/binder-examples/jupyter-extension/master?filepath=index.ipynb)

This example demonstrates how to enable Jupyter extensions with Binder. We'll
cover a few in this repo because some are idiosyncratic in how they're enabled.

We accomplish each using a `requirements.txt` file to install the extensions,
then a `postBuild` file to enable them.

## ipywidgets

Ipywidgets lets you create interactive widgets in your notebook.
Installation is fairly straightforward. You install the python package,
then enable the extension.

## python-markdown
The `python-markdown` extension is useful for interweaving computational
cells (e.g., python cells) and markdown cells. As this extension automatically
runs code in the notebook, you need to be sure to "trust" the notebooks in your
`postBuild` script (see the script in this repo for example).
