# Pan-genome analyses of model Fungal species.

**Charley G. P. McCarthy & David A. Fitzpatrick (submitted).**

This repository holds custom pipelines used to analyse the pan-genomes of four model fungal species; *Saccharomyces cerevisiae*, *Candida albicans*, *Cryptococcus neoformans* var. *grubii* and *Aspergillus fumigatus*.

The pipelines are as follows:
+ A custom gene model prediction pipeline which uses parallelized `Exonerate` searches, `GeneMark-ES` HMM prediction and `TransDecoder` coding potential prediction to generate gene model sets for each strain genome in a pan-genome dataset.

+ A post-processing pipeline which takes the results of PanOCT output and attempts to merge non-core syntenic clusters of gene models which have reciprocal sequence similarity between each other but have otherwise lost microsynteny using iterative BLAST+ searches and parsing. This pipeline also runs two R scripts to generate ring charts of the size of species core and accessory genomes as well as an UpSet distribution of accessory gene model clusters within pan-genomes.

## Requirements

Each analysis in McCarthy & Fitzpatrick (in revision) using these pipelines was performed on a HPC cluster with a PBS scheduler. These pipelines have also been tested in other Linux and macOS environments.

- Python
  - Biopython

- R
  - Cairo
  - UpSetR
  - ggplot2
  - ggrepel

- BLAST+

- [Exonerate](https://www.ebi.ac.uk/about/vertebrate-genomics/software/exonerate)

- GeneMark-ES

- TransDecoder
