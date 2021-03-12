# Wgs sample qc environment setup

## Environment Setup Instructions

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

## Test Run (juno)

```
wgs sample_qc --input_yaml /juno/work/shah/abramsd/CODE/wgs_genome_qc_TESTRUNS/input.yaml --out_dir out --tmpdir tmp --refdir /juno/work/shah/users/grewald/TWINS_NEW_DATA/WGS_REFERENCE --submit local --loglevel DEBUG --nocleanup
```

## Example Input Yaml

```
SPECTRUM-OV-036_0.1.0:
  breakpoints_consensus: /juno/work/shah/abramsd/CODE/wgs_genome_qc_TESTRUNS/0.1.0_data/SPECTRUM-OV-036_S1_BOWEL_filtered_consensus_calls.csv
  germline_calls: /juno/work/shah/abramsd/CODE/wgs_genome_qc_TESTRUNS/0.1.0_data/SPECTRUM-OV-036_cosensus_germline_small.maf
  normal_bam: /juno/work/shah/abramsd/CODE/wgs_genome_qc_TESTRUNS/data/normal.bam
  remixt: /juno/work/shah/abramsd/CODE/wgs_genome_qc_TESTRUNS/0.1.0_data/SPECTRUM-OV-036_S1_BOWEL_remixt.h5
  #roh: /juno/work/shah/isabl_data_lake/analyses/82/69/8269/results/germline/SPECTRUM-OV-107_BC1_NORMAL_R1/SPECTRUM-OV-107_BC1_NORMAL_R1_roh.csv.gz
  roh: /juno/work/shah/abramsd/CODE/wgs_genome_qc_TESTRUNS/0.1.0_data/SPECTRUM-OV-036_BC1_NORMAL_R1_roh.csv
  somatic_calls: /juno/work/shah/abramsd/CODE/wgs_genome_qc_TESTRUNS/0.1.0_data/SPECTRUM-OV-036_S1_BOWEL_consensus_somatic.maf
  titan: /juno/work/shah/abramsd/CODE/wgs_genome_qc_TESTRUNS/0.1.0_data/SPECTRUM-OV-036_S1_BOWEL_titan_markers.csv.gz
  tumour_bam: /juno/work/shah/abramsd/CODE/wgs_genome_qc_TESTRUNS/data/tumour.bam
```

## Outputs:

```
{sample_id}_genome_wide.pdf
```
