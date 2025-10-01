# Installation of opendvp

## Quick start

```console
$ conda create --name opendvp -y python=3.12
$ conda activate opendvp
$ pip install opendvp
```

or

```bash
$ uv add opendvp
```

## Installing opendvp with conda-like (environment manager)

Mamba is a fast, drop-in replacement for the conda package manager. It significantly speeds up installing packages and resolving environment dependencies, making it a great tool for any data scientist or Python developer. 🐍

This tutorial will guide you through installing Mamba on your system.

If you are new here is a nice post explaining the main [Concepts](https://mamba.readthedocs.io/en/latest/user_guide/concepts.html#concepts) (<5min read)

### Install environment manager

1. Check and download the most recent `Conda-forge Installer` release for your OS here: [Downloads](https://conda-forge.org/download/).
2. Follow instructions on website for your OS
3. For Windows only: use the Miniforge Prompt
4. Run `conda init`
5. Run `conda install mamba -n base -c conda-forge` to install mamba

### Install opendvp

```console
$ conda create --name opendvp -y python=3.12
$ conda activate opendvp
$ pip install opendvp
```

### Test install

```console
$ python
>>> import opendvp
>>> print(opendvp.__version__)
0.7.1
```

## Installing opendvp with uv

Assuming that most proteomics analysts use R, I have made this small tutorial to get you started with environment creation in python. `uv` is an extremely fast Python package and project manager, it has many great features and it is a great skill to have if you need python for anything. Check their [documentation](https://docs.astral.sh/uv/).

### Installing uv in Windows

Use this line to download the latest stable `uv` version

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

Unfortunately, there are many things that can go wrong in this step, depending on your computer setup. I am afraid I cannot explain all of these. I suggest you ask ChatGPT for help :)

### Installing uv in Linux and MacOS

Use curl to download the script and execute it with sh:

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

or brew

```bash
brew install uv
```

#### Check uv works by running `uv` in the command line

```console
$ uv
An extremely fast Python package manager.

Usage: uv [OPTIONS] <COMMAND>

Commands:
  run      Run a command or script
  init     Create a new project
  add      Add dependencies to the project
  remove   Remove dependencies from the project
  version  Read or update the project's version
  sync     Update the project's environment
  lock     Update the project's lockfile
  export   Export the project's lockfile to an alternate format
  tree     Display the project's dependency tree
  tool     Run and install commands provided by Python packages
  python   Manage Python versions and installations
  pip      Manage Python packages with a pip-compatible interface
  venv     Create a virtual environment
  build    Build Python packages into source distributions and wheels
  publish  Upload distributions to an index
  cache    Manage uv's cache
  self     Manage the uv executable
  help     Display documentation for a command
```

## Install opendvp with `uv`

1. Create a new directory.

`uv` works by creating directory specific environments. Therefore you should create a new directory for each different project. This might seems like separating a lot of things, but will keep your proyects tidy, and you should only have what you need for each specific project.

2. Open directory in [VSCode](https://code.visualstudio.com/download)

3. Use `uv` to create your python environment

```console
$ uv init --python 3.12
Initialized project `temp`
```

4. Use `uv` to install opendvp

```console
$ uv add opendvp
```

### Check opendvp is installed

```bash
> uv pip list | grep opendvp
opendvp                       0.7.0
```

Showing you what version is installed.

## Use openDVP with jupyter notebooks

- Create a new jupyter notebook, or a new file with suffix `.ipynb`
- Choose `Select kernel` in VSCode, and pick the `Python environment` that matches your directory name.

Try importing opendvp, it will take some time the first time you do this.

```python
import opendvp as dvp
```

Use this to check the version from within python

```python
print(dvp.__version__)
```

## Troubleshooting

- Python version cannot be >=3.13 ; this will cause install to fail. Use python 3.11 or 3.12.