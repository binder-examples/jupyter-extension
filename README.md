# Enabling Jupyter Extensions with post-build commands

[![Binder](https://beta.mybinder.org/badge.svg)](https://beta.mybinder.org/v2/gh/binder-examples/jupyter-extension/master?filepath=index.ipynb) jupyter notebook

[![Binder](https://beta.mybinder.org/badge.svg)](https://beta.mybinder.org/v2/gh/binder-examples/jupyter-extension/master?urlpath=lab) jupyter lab


This example demonstrates how to enable Jupyter extensions with Binder. We'll
cover a few in this repo because some are idiosyncratic in how they're enabled.

We accomplish each using a `requirements.txt` file to install the extensions,
then a `postBuild` file to enable them.

## ipywidgets

Ipywidgets lets you create interactive widgets in your notebook.
Installation is fairly straightforward. You install the python package,
then enable the extension.

JupyterLab requires installing a jupyter labextension.

## postBuild
Drop support for python-markdown which does not work with jupyterlab (at least as of 0.35.4)

[Match jupyterlab-manager version to jupyterlab 0.35.4](https://github.com/jupyter-widgets/ipywidgets/tree/master/packages/jupyterlab-manager#version-compatibility)
```bash
jupyter labextension install @jupyter-widgets/jupyterlab-manager@0.38
```
