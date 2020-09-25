# Introduction
This repository contains R scripts used for our publication Kinase deficient NTRK2 splice variant, TrkB.T1, links development and oncogenesis"

## References 

1) Cao, J., Spielmann, M., Qiu, X. et al. The single-cell transcriptional landscape of mammalian organogenesis. Nature 566, 496–502 (2019). https://doi.org/10.1038/s41586-019-0969-x
2) Anders, S., Pyl, P. T., & Huber, W. (2015). HTSeq--a Python framework to work with high-throughput sequencing data. Bioinformatics (Oxford, England), 31(2), 166–169. https://doi.org/10.1093/bioinformatics/btu638
3) Trapnell C. et. al. The dynamics and regulators of cell fate decisions are revealed by pseudotemporal ordering of single cells. Nat. Biotechnol. 32, 381–386 (2014). https://doi.org/10.1038/nbt.2859
4) Qiu, X. et. al. Reversed graph embedding resolves complex single-cell trajectories. Nat. Methods 14, 979–982 (2017). https://doi.org/10.1038/nmeth.4402
5) McInnes, L., Healy, J. & Melville, J. UMAP: Uniform Manifold Approximation and Projection for dimension reduction. Preprint at https://arxiv.org/abs/1802.03426 (2018).
6) Vivian J, Rao AA, Nothaft FA, et al. (2017) Toil enables reproducible, open source, big biomedical data analyses. Nature biotechnology. 
7) R Core Team (2018). R: A language and environment for statistical computing. R Foundation for Statistical Computing, Vienna, Austria. URL https://www.R-project.org/.

## Tools used for analysis 

All our analysis is done in R using the following  R/Biocondcutor packages.

1) [ggplot2](https://ggplot2.tidyverse.org/) for making plots in our paper. 
2) [htseq-count](https://htseq.readthedocs.io/en/release_0.11.1/count.html) for estimating transcript expression data 
3) [Monocle3](https://cole-trapnell-lab.github.io/monocle3/) for normalizing trasncript expression data
4) [rtracklyer](https://bioconductor.org/packages/release/bioc/html/rtracklayer.html) to import the GTF file downloaded from Gencode (v M12)

Monocle3 can be installed using instructions found [here](https://cole-trapnell-lab.github.io/monocle3/docs/installation/)

To ensure smooth execution of code in this repository, please install the 
following packages 

```{r eval=FALSE}
if (!requireNamespace("BiocManager", quietly = TRUE))
    install.packages("BiocManager")
BiocManager::install(c( "rtracklyer", "ggplot2", "gridExtra"))
```

## Download publicly available files

1) SAM alignment files for the MOCA dataset were downloaded from [here](https://shendure-web.gs.washington.edu/content/members/cao1025/public/nobackup/)
2) “cell_annotation.csv” which contained TSNE coordinates, UMAP coordinates, and information about clusters and trajectories was downloaded from [here](https://oncoscape.v3.sttrcancer.org/atlas.gs.washington.edu.mouse.rna/downloads)
3) “Comprehensive gene annotation” file was downloaded from [Gencode](https://www.gencodegenes.org/mouse/release_M12.html)
4) Transcript data (TPM data) was downloaded for TARGET from [UCSC Xena](https://xenabrowser.net/datapages/?dataset=target_RSEM_gene_tpm&host=https%3A%2F%2Ftoil.xenahubs.net&removeHub=https%3A%2F%2Fxena.treehouse.gi.ucsc.edu%3A443)
5) Transcript Data (TCGA RNAseqV2 RSEM data) for each TCGA organ sites was downloaded from here(https://gdac.broadinstitute.org/). 
