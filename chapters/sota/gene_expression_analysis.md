### Gene Expression Analysis

The most recurring task in research & early development is the gene expression analysis on a given date source.

#### Methods for differential gene expression

Gene expression methods usually utilize 

Name | Strategy | Prefered Input Data
-----|------------|--------------------
[edgeR](http://doi.org/10.1093/bioinformatics/btp616) | <ul><li>Assume that most genes are not differentially expressed </li><li>item2</li></ul>| RNAseq
DEseq | Assume that most genes are not differentially expressed | RNAseq
limma | a| microarray


#### Methods for batch-effect correction in meta-analysis

#### Methods for gene-set/pathway enrichment analysis

* Methods for differential gene expression: edgeR/DEseq/limma. It will be automatically chosen based on data type; users can rely on the system's choice.
* : ComBat, SVA, and BioQC. Here we will probably have to compare different methods and reach a conclusion.
* : CAMERA/Fisher's exact test/BioQC.
Previously we found out that CAMERA and BioQC will lead to false negatives when many genes are differentially expressed, while Fisher's exact test will not (not published). We can verify this and make a meta-method to accommodate different scenarios.