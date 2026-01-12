# Spen–Su(H) interaction mapping using FragFold and ColabFold

This repository contains the computational pipeline, parameters, and
processed results used to identify candidate Spen peptide segments
that potentially interact with the C-terminal domain (CTD) of
Suppressor of Hairless [Su(H)].

## Scientific background
Spen is a large transcriptional coregulator enriched in intrinsically
disordered regions (IDRs). Unlike Hairless, which binds Su(H) via a
single well-defined structural motif, Spen is hypothesized to engage
Su(H) through multiple weak or transient interaction hotspots.
To systematically explore this possibility, we performed a sliding-window
structure prediction screen using FragFold and ColabFold.

## What is included in this repository
- Fully specified FragFold/Nextflow parameter files (`params/`)
- Modified pipeline configuration (`config/nextflow.config`)
- Scripts for ranking and visualizing interaction confidence
- Processed summary results (ipTM distributions and hotspot plots)
- Representative predicted structures for top candidate regions

## What is NOT included
- Full ColabFold raw outputs (thousands of directories)
- Conda environments or AlphaFold databases

These are provided separately as a reproducible environment snapshot
via GitHub Releases.

## Reproducibility
A complete runnable environment snapshot is available under
**GitHub Releases (env-v1)**. See `ENVIRONMENT.md` for step-by-step
instructions to reproduce the computational results.

## Key results overview
The screening reveals multiple Spen regions with elevated predicted
interface confidence (ipTM), most prominently around residues
~4690–4730 and ~5230–5270, consistent with a multi-hotspot interaction
model.

## Citation
If you use this repository, please cite:
[Manuscript reference or preprint placeholder]
