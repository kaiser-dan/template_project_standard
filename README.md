# Project Template

Research project DOING WHAT.

The repository contains the original scientific analyses developed by the Authors (see below) for the paper

- **(In preparation)** LastName, FirstName. Year. [Paper title](arxiv.org).

If you use this repository in any fashion in your own work, please cite our work according to the `CITATION.cff`.

# Contents

- [Project Template](#project-template)
- [Contents](#contents)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installing](#installing)
  - [Quick Start](#quick-start)
- [Usage](#usage)
  - [Reproducing experiments](#reproducing-experiments)
  - [Applying to new data](#applying-to-new-data)
- [Documentation](#documentation)
- [Tests](#tests)
- [Other Information](#other-information)
  - [Built With](#built-with)
  - [Versioning](#versioning)
  - [Authors](#authors)
  - [License](#license)
  - [Acknowledgments](#acknowledgments)

# Getting Started

The code base for this project is written in Python with package management handled with [`uv`](https://docs.astral.sh/uv/).

These instructions will give you a copy of the project up and running on
your local machine for development, testing, and analysis purposes.

## Prerequisites

A compatible Python install is needed to begin - the package management is handled by [`uv`](https://docs.astral.sh/uv/) as described below.

See the [`uv` installation instructions](https://docs.astral.sh/uv/getting-started/installation/) and make sure you have a working installation on your system before proceeding.

Optionally, if you prefer command runners in the GNUMake style, we've included a simple [`justfile`](https://github.com/casey/just).

## Installing

To (locally) reproduce this project, do the following:

1. Clone this repository. Notice that raw data are typically not included in the git-history and may need to be downloaded independently - see [Reproducing Experiments](#reproducing-experiments) for more information.
2. Create a virtual environment with the necessary packages. Using `uv`, this can be done with the single command run from the root directory:

```bash
uv sync
```

3. (Optional) If you want to reproduce the experiments using our original [`snakemake`](https://snakemake.readthedocs.io/en/stable/) workflow, install additional dependencies with the command:

```bash
uv sync --group workflow
```

This will install all necessary packages and place them into a virtual environment, by default located at `./.venv/`.
To use the install package, either prefix all commands with `uv run` (preferred) - e.g., `uv run python --version` - or first activate the environment with `source .venv/bin/activate` (if on Unix-based system, `source .venv/Scripts/activate` if on Windows).

## Quick Start

The Jupyter notebook [`example.ipynb`](example.ipynb) contains a short working example and some comments to illustrate the basic usage of the developed method.

If you have followed the installation instructions above, you can open the notebook with the following command executed from the repository root:

```bash
uv run --with jupyter jupyter lab example.ipynb
```

This will open a Jupyter lab instance in your default browser.

# Usage

## Reproducing experiments

1. GET DATA
2. RUN EXPERIMENTS
3. ANALYZE

## Applying to new data

1. INSTRUCTIONS

# Documentation

This repository does not maintain extensive independent documentation for its source code. Functions have docstrings where needed and the [`example.ipynb`](example.ipynb) file can be used as a user guide.

# Tests

All unit tests are written with [pytest](docs.pytest.org).

Tests can be run directly with the commands:

```bash
uv run --extra dev pytest
```

# Other Information

## Built With

### Repository and Version Control

- [ChooseALicense](https://choosealicense.com/) - Used to choose the license.
- [Commitizen]() - Used to maintain Conventional Commit standard.

### Source code

- [BeautifulSoup]() - Used for retrieving arXiv tags.

### Research analysis

- [Snakemake]() - Used for organizing and running research pipeline.
- [Quarto]() - Used for writing analyses documents.

## Versioning

We use [Semantic Versioning](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/kaiser-dan/higher-order_multiplex_reconstruction/tags) and our [published releases](https://github.com/kaiser-dan/higher-order_multiplex_reconstruction/releases).

> This repository is primarily intended to promote reproducibility and extensibility of a specific set of scientific analyses.
> There will likely be very few released versions, and the current release *should always be preferred if you want to apply the methodology to your own data*!

## Authors

All correspondence should be directed to [CORRESPONDING AUTHOR](mailto:email@iu.edu).

- AUTHOR
- AUTHOR
- AUTHOR

## License

This project is licensed under the [MIT License](LICENSE.md) Creative Commons License - see the [LICENSE](LICENSE.md) file for details.

## Acknowledgments

- **Billie Thompson** - *Provided original README* - [PurpleBooth](https://github.com/PurpleBooth)
- **George Datseris** - *Published workshop on scientific code; inspired organization for reproducibility* - [GoodScientificCodeWorkshop](https://github.com/JuliaDynamics/GoodScientificCodeWorkshop)

