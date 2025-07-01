# openDVP - community empowered Deep Visual Proteomics


`opendvp` is a python package containing different tools enabling users to perform deep visual proteomics. To perform quality control and image analysis of multiplex immunofluorescence. Also to integrate imaging datasets with proteomic datasets with [Spatialdata](https://github.com/scverse/spatialdata). Lastly, it contains a powerful toolkit for label-free downstream proteomic analysis.

It is a package that leverages the [scverse]() ecosystem, designed for easy interoperability with `anndata`, `scanpy`, `decoupler`, `scimap`, and other related packages.

## Getting started

Please check our [API documentation](api/index.md) for detailed functionalities.

## Installation

You need at least Python 3.10 installed. If you do not have Python installed, we suggest installing via [uv](https://github.com/astral-sh/uv).  

There are three alternatives to install openDVP:  
1. Install the latest stable release from [PyPI](https://pypi.org/project/openDVP/) with minimal dependencies:
```bash
pip install openDVP
```
2. Install the latest stable release from [PyPI](https://pypi.org/project/openDVP/) with spatialdata capabilities:
```bash
pip install 'openDVP[spatialdata]'
```
3. Install the latest development version from github:
```bash
pip install git+https://github.com/CosciaLab/openDVP.git@main
```

## Tutorials



## Contact

For questions about openDVP and the DVP workflow you are very welcome to post a message in the [discussion board](https://github.com/CosciaLab/openDVP/discussions). For issues with the software, please post issues on [Github Issues](https://github.com/CosciaLab/openDVP/issues).

## Citation

Not yet available.


```{toctree}
:maxdepth: 2
:hidden:

api/index
Tutorials/index
references
```