# BRB-seq
Code and scripts for reproducing figures of BRB-seq paper

# Raw .fastq datasets
RNA-seq raw data (fastq files) are accessible in ArrayExpress under accession numbers [E-MTAB-6469](https://www.ebi.ac.uk/arrayexpress/experiments/E-MTAB-6469/), [E-MTAB-6984](https://www.ebi.ac.uk/arrayexpress/experiments/E-MTAB-6984/) and [E-MTAB-7524](https://www.ebi.ac.uk/arrayexpress/experiments/E-MTAB-7524/). TruSeq datasets on LCL GBR samples from the 1000 Genomes project were downloaded from ArrayExpress [E-MTAB-3656](https://www.ebi.ac.uk/arrayexpress/experiments/E-MTAB-3656/) and [E-GEUV-1](https://www.ebi.ac.uk/arrayexpress/experiments/E-GEUV-1/) respectively. The public SCRB-seq datasets were from Hafner *et al.* ([GSE80297](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE80297)); Cacchiarelli *et al.* ([GSE62777](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE62777)); Kilens *et al.* ([PRJEB18663](https://www.ebi.ac.uk/ena/data/view/PRJEB18663)) and Xiong *et al.* ([GSE98432](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE98432)).

# Count matrices
The sequencing reads were aligned to the Ensembl r87 gene annotation of the hg38 genome using STAR (version 2.5.3a). Then, using the [BRB-seqTools suite](http://github.com/DeplanckeLab/BRB-seqTools), we performed simultaneously the second demultiplexing and the count of reads/transcripts (UMI) per gene from the R1 FASTQ and the aligned R2 BAM files. This generated two count matrices (reads and UMI) that were used for further analyses. In the case of TruSeq, count matrices were generated with HTSeq (version 0.9.1).
> **Note:** Count matrices used in the scripts were deposited on this GitHub page, in the [**data**](https://github.com/DeplanckeLab/BRB-seq/tree/main/data) folder

# Tool for full analyses of BRB-seq datasets
The [BRB-seqTools suite](http://github.com/DeplanckeLab/BRB-seqTools) is implemented in Java. The version used in the manuscript (source code and tool) is permanently available under https://doi.org/10.5281/zenodo.2552405. It supports all the required post-sequencing tasks (alignment, counts) up until the generation of the read/UMI count matrix.
> **Of note:** Now, it's rather recommended to use STARsolo for performing the same tasks

# Citation and link to paper
[Alpern D., Gardeux V. Russeil, J. *et al.* BRB-seq: ultra-affordable high-throughput transcriptomics enabled by bulk RNA barcoding and sequencing. *Genome Biol* **20**, 71 (2019)](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-019-1671-x)
