
# Wgs sample qc environment setup
## Requirements
The requirements for the environment are in `requirements_conda.txt` and `requirements_pip.txt`

Just create environment with `conda create` and install the requirements with `pip install`

## R setup

To install the required R packages, run:
```
conda install -c conda-forge r-circlize
conda install -c bioconda bioconductor-complexheatmap
conda install -c r r-rcolorbrewer
conda install -c anaconda readline
conda install -c r r
```

## R script

download `https://github.com/shahcompbio/conda-recipes/blob/master/circos_utils/scripts/circos.R`

