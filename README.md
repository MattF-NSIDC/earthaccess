# earthdata
### A NASA CMR/EDL client library

<p align="center">
    <em>A summary phrase to catch attention!</em>
</p>

<p align="center">
<a href="https://github.com/betolink/earthdata/actions?query=workflow%3ATest" target="_blank">
    <img src="https://github.com/betolink/earthdata/workflows/Test/badge.svg" alt="Test">
</a>
<a href="https://github.com/betolink/earthdata/actions?query=workflow%3APublish" target="_blank">
    <img src="https://github.com/betolink/earthdata/workflows/Publish/badge.svg" alt="Publish">
</a>
<a href="https://dependabot.com/" target="_blank">
    <img src="https://flat.badgen.net/dependabot/betolink/earthdata?icon=dependabot" alt="Dependabot Enabled">
</a>
<a href="https://codecov.io/gh/betolink/earthdata" target="_blank">
    <img src="https://img.shields.io/codecov/c/github/betolink/earthdata?color=%2334D058" alt="Coverage">
</a>
<a href="https://pypi.org/project/earthdata" target="_blank">
    <img src="https://img.shields.io/pypi/v/earthdata?color=%2334D058&label=pypi%20package" alt="Package version">
</a>
<a href="https://pypi.org/project/earthdata/" target="_blank">
    <img src="https://img.shields.io/pypi/pyversions/earthdata.svg" alt="Python Versions">
</a>


## Overview


## Installing earthdata

Install the latest release:

```bash
pip install earthdata
```

Or you can clone `earthdata` and get started locally

```bash

# ensure you have Poetry installed
pip install --user poetry

# install all dependencies (including dev)
poetry install

# develop!

```

## Example Usage

```python
from earthdata import auth, search

auth.login('user', 'password')

collections = search.collections(params)
collections

granules = search.granules(params)
granules

granules.size() # total size of the granules
granules.data_links() # -> you can now pass this to xarray
granules.download(10, './data') # will download 10 granules

# do stuff
```

Only **Python 3.6+** is supported as required by the black, pydantic packages


## Contributing Guide

Welcome! 😊👋

> Please see the [Contributing Guide](CONTRIBUTING.md).
