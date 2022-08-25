<div>
  <img src="https://raw.githubusercontent.com/TGSAI/mdio.github.io/gh-pages/assets/images/mdio.png",
width=200"><br>
</div>

[![PyPI](https://img.shields.io/pypi/v/multidimio.svg)][pypi_]
[![Status](https://img.shields.io/pypi/status/multidimio.svg)][status]
[![Python Version](https://img.shields.io/pypi/pyversions/multidimio)][python version]
[![License](https://img.shields.io/pypi/l/multidimio)][license]

[![Read the documentation at https://mdio-python.readthedocs.io/](https://img.shields.io/readthedocs/mdio-python/latest.svg?label=Read%20the%20Docs)][read the docs]
[![Tests](https://github.com/TGSAI/mdio-python/workflows/Tests/badge.svg)][tests]
[![Codecov](https://codecov.io/gh/TGSAI/mdio-python/branch/main/graph/badge.svg)][codecov]

[![pre-commit](https://img.shields.io/badge/pre--commit-enabled-brightgreen?logo=pre-commit&logoColor=white)][pre-commit]
[![Black](https://img.shields.io/badge/code%20style-black-000000.svg)][black]

[pypi_]: https://pypi.org/project/multidimio/
[status]: https://pypi.org/project/multidimio/
[python version]: https://pypi.org/project/multidimio
[read the docs]: https://mdio-python.readthedocs.io/
[tests]: https://github.com/TGSAI/mdio-python/actions?workflow=Tests
[codecov]: https://app.codecov.io/gh/TGSAI/mdio-python
[pre-commit]: https://github.com/pre-commit/pre-commit
[black]: https://github.com/psf/black

**_"MDIO"_** is a library to work with large multidimensional energy datasets.
The primary motivation behind **MDIO** is to represent multidimensional
time series data in a format that makes it easier to use in resource assessment,
machine learning, and data processing workflows.

See the [documentation][read the docs] for more information.

# Features

**Shared Features**

- Abstractions for common energy data types (see below).
- Cloud native chunked storage based on [Zarr][zarr] and [fsspec][fsspec].
- Lossy and lossless data compression using [Blosc][blosc] and [ZFP][zfp].
- Distributed reads and writes using [Dask][dask].
- Powerful command-line-interface (CLI) based on [Click][click]

**Domain Specific Features**

- Oil & Gas Data
  - Import and export 2D - 5D seismic data types stored in SEG-Y.
  - Import seismic interpretation, horizon, data. **FUTURE**
  - Optimized chunking logic for various seismic types. **FUTURE**
- Wind Resource Assessment
  - Numerical weather prediction models with arbitrary metadata. **FUTURE**
  - Optimized chunking logic for time-series analysis and mapping. **FUTURE**
  - [Xarray][xarray] interface. **FUTURE**

The features marked as **FUTURE** will be open-sourced at a later date.

# Installing MDIO

Simplest way to install _MDIO_ via [pip] from [PyPI]:

```shell
pip install multidimio
```

For more instructions, please see the [installation instructions][read the docs]
in the documentation.

# Using MDIO

Please see the [Command-line Reference][usage] for details.

For Python API please see the [API Reference] for details.

# Requirements

### Minimal

Chunked storage and parallelization: `zarr`, `dask`, `numba`, and `psutil`.\
SEG-Y Parsing: `segyio`\
CLI and Progress Bars: `click`, `click-params`, and `tqdm`.

### Optional

Distributed computing `[distributed]`: `distributed` and `bokeh`.\
Cloud Object Store I/O `[cloud]`: `s3fs`, `gcsfs`, and `adlfs`.\
Lossy Compression `[lossy]`: `zfpy`

# Contributing to MDIO

Contributions are very welcome.
To learn more, see the [Contributor Guide].

# Licensing

Distributed under the terms of the [Apache 2.0 license][license],
_MDIO_ is free and open source software.

# Issues

If you encounter any problems,
please [file an issue] along with a detailed description.

# Credits

This project was established at [TGS](https://www.tgs.com/). Original authors
and current maintainers are [Altay Sansal](https://github.com/tasansal) and
[Sri Kainkaryam](https://github.com/srib); with the support of many more great
colleagues.

This project template is based on [@cjolowicz]'s [Hypermodern Python Cookiecutter]
template.

[@cjolowicz]: https://github.com/cjolowicz
[pypi]: https://pypi.org/
[hypermodern python cookiecutter]: https://github.com/cjolowicz/cookiecutter-hypermodern-python
[file an issue]: https://github.com/TGSAI/mdio-python/issues
[pip]: https://pip.pypa.io/
[dask]: https://www.dask.org/
[zarr]: https://zarr.dev/
[fsspec]: https://filesystem-spec.readthedocs.io/en/latest/
[s3fs]: https://s3fs.readthedocs.io/
[gcsfs]: https://gcsfs.readthedocs.io/
[adlfs]: https://github.com/fsspec/adlfs
[blosc]: https://www.blosc.org/
[zfp]: https://computing.llnl.gov/projects/zfp
[xarray]: https://xarray.dev/
[click]: https://palletsprojects.com/p/click/

<!-- github-only -->

[license]: https://github.com/TGSAI/mdio-python/blob/main/LICENSE
[contributor guide]: https://github.com/TGSAI/mdio-python/blob/main/CONTRIBUTING.md
[usage]: https://mdio-python.readthedocs.io/en/latest/usage.html
[api reference]: https://mdio-python.readthedocs.io/en/latest/reference.html
[install]: https://mdio-python.readthedocs.io/en/latest/installation.html
