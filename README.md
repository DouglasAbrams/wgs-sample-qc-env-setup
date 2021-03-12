# Wgs sample qc environment setup

## Instructions

Create a conda environment with the conda requirements at `conda_env_path`:
```
create --file https://raw.githubusercontent.com/DouglasAbrams/wgs-sample-qc-env-setup/main/conda_requirements.txt --prefix {conda_env_path}
```

Activate the environment:
```
conda activate {conda_env_path}
```

Install pip reqs:
```
pip install -r https://raw.githubusercontent.com/amcpherson/wgs-sample-qc-env-setup/main/requirements_pip.txt
```

## Test run (juno

```
wgs sample_qc --input_yaml /juno/work/shah/abramsd/CODE/wgs_genome_qc_TESTRUNS/input.yaml --out_dir out --tmpdir tmp --refdir /juno/work/shah/users/grewald/TWINS_NEW_DATA/WGS_REFERENCE --submit local --loglevel DEBUG --nocleanup
```
