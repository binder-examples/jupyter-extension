# Enabling Jupyter Extensions with post-build commands

[![Binder](https://mybinder.org/badge_logo.svg)](https://beta.mybinder.org/v2/gh/binder-examples/jupyter-extension/master?filepath=index.ipynb) (Jupyter Notebook)

[![Binder](https://mybinder.org/badge_logo.svg)](https://beta.mybinder.org/v2/gh/binder-examples/jupyter-extension/master?urlpath=lab) (Jupyter Lab)


This example demonstrates how to enable Jupyter extensions with Binder. We'll
cover a few in this repo because some are idiosyncratic in how they're enabled.

We accomplish each using a `requirements.txt` file to install the extensions,
then a `postBuild` file to enable them.

## ipywidgets

Ipywidgets lets you create interactive widgets in your notebook.
Installation is fairly straightforward. You install the python package,
then enable the extension.

The postBuild file defines commands (one per line) to be run with bash.
In this case, we use it to install a Jupyter Lab extension
(by calling jupyter labextension) which allows ipywidgets
to be displayed within notebooks.
