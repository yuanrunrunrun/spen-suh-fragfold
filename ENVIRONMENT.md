# Reproducible Computational Environment

This project relies on a pre-configured computational environment
to ensure full reproducibility of the FragFold–ColabFold screening.

## Environment snapshot
A full environment snapshot is provided via GitHub Releases
(tag: `env-v1`) and includes:

- FragFold repository (with local modifications)
- LocalColabFold
- Miniconda3 with all Python dependencies
- AlphaFold/ColabFold parameter databases

Due to GitHub file size limits, the snapshot is split into multiple parts.

## Download and reconstruction

```bash
# Download all parts and checksum
wget https://github.com/yuanrunrunrun/spen-suh-fragfold/releases/download/env-v1/spen_stack.tar.gz.part_000
wget https://github.com/yuanrunrunrun/spen-suh-fragfold/releases/download/env-v1/spen_stack.tar.gz.part_001
# ... repeat for all parts
wget https://github.com/yuanrunrunrun/spen-suh-fragfold/releases/download/env-v1/spen_stack.tar.gz.sha256

# Reassemble
cat spen_stack.tar.gz.part_* > spen_stack.tar.gz


# Extract (must be extracted to root directory)
sudo tar -xzf spen_stack.tar.gz -C /


## Activate environment

```bash
source /root/miniconda3/etc/profile.d/conda.sh
conda activate fragfold
```

## Hardware requirements

* GPU: NVIDIA RTX 3090 / 4090 or equivalent
* VRAM: ≥24 GB recommended
* Disk space: ≥100 GB free
* OS: Linux (tested on Ubuntu 22.04)

## Re-running the pipeline

Example command:

```bash
nextflow run FragFold/nextflow/main.nf \
  -c FragFold/nextflow/nextflow.config \
  -params-file FragFold/nextflow/params/spen_suh.yaml
```

```

---



