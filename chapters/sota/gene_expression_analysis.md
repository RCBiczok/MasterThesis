### Gene Expression Analysis

The most recurring task in pharmaceutical research & early development is the gene expression analysis on a given date source. 

#### Methods for differential gene expression inferrence

Name | Strategy | Prefered Input Data
-----|------------|--------------------
[edgeR](http://doi.org/10.1093/bioinformatics/btp616) | Negative binomial distribution + Trimmed Mean of M values (TMM) Normalization | RNAseq
[DEseq](https://doi.org/10.1186/s13059-014-0550-8) | Negative binomial distribution + scaling factor normalization procedure | RNAseq
[limma](https://doi.org/10.1093/nar/gkv007) | Linear Modeling + voom transformation of counts (vor RNAseq) | RNAseq & microarray

The "rule of thumb" is to use limma for microarray data and edgeR for RNAseq data. DEseq is used to verify that a hypothesis based on edgeR results can also be derived from DEseq results (since edgeR is known to report more false positives).

#### Methods for batch-effect correction in meta-analysis

We use ComBat, SVA, and BioQC. Here we will probably have to compare different methods and reach a conclusion.

#### Methods for gene-set/pathway enrichment analysis

We use CAMERA, BioQC, and Fisher's exact test.
Previously we found out that CAMERA and BioQC will lead to false negatives when many genes are differentially expressed, while Fisher's exact test will not (not published). We can verify this and make a meta-method to accommodate different scenarios.