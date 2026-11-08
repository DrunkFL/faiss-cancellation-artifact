# Cancellation in Faiss Search on Multicore Processors

Research artifact for the study by Dongze Li and Jiahui Liu. Download and extract Faiss_Cancellation_Artifact_v1.zip. Run the commands below from the extracted directory containing analysis/. Python 3.12 and its standard library are sufficient. Use a fresh output directory for each run.

### Reproduce the public-threshold tables

```sh
python -B analysis/recompute_public_threshold.py --output reproduced
python -B analysis/joint_directions.py public-threshold/analysis/block_comparisons.csv public-threshold/analysis/process_medians.csv joint-check/joint_directions_outer16.csv
```

The first command checks six tables against the archived measurements (768 processes, 4,608 formal timing records). The second reconstructs Table V15 across 96 blocks. Compare its CSV with public-threshold/analysis/joint_directions_outer16.csv.

The archive also includes historical table and figure inputs in document/data, CPU4 summaries in historical/CPU4, and source changes for the historical and modern experiments. See INPUTS_AND_LICENSES.md for vector provenance, preparation, exclusions and license notices. Additional evidence for historical experiments is supplied in Supporting Information S2.
