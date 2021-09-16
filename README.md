# Enabling Jupyter Extensions with post-build commands

[![Binder](https://mybinder.org/badge_logo.svg)](https://beta.mybinder.org/v2/gh/binder-examples/jupyter-extension/HEAD?urlpath=/tree/index.ipynb) (Jupyter Notebook)

[![Binder](https://mybinder.org/badge_logo.svg)](https://beta.mybinder.org/v2/gh/binder-examples/jupyter-extension/HEAD?urlpath=lab/tree/index.ipynb) (Jupyter Lab)


This example demonstrates how to enable Jupyter extensions with Binder.We currently only cover one example
in this repo. Be aware that some are idiosyncratic in how they're enabled.

We accomplish each step using a `requirements.txt` file to install the extension,
then a `postBuild` file to enable it.

## ipywidgets

Ipywidgets lets you create interactive widgets in your notebook.
Installation is fairly straightforward. You install the python package,
then enable the extension.

The postBuild file defines commands (one per line) to be run with bash.
In this case, we first enable the ipywidgets extension in the classic notebook interface. We then use it to install a Jupyter Lab extension
(by calling jupyter labextension) which allows ipywidgets
to be displayed within notebooks.
