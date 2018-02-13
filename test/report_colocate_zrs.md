#Research Report for Co-locate RNA transcripts 

## Ruosi Zhang

###**Description**: 

The report is about co-locate RNA transcripts identified by ISO-seq of iPSC, S1 and S2 cells with stage-specific open chromatin domains identified by ATAC-Seq.

###**Steps**:

1) Get all the genes that ISO-seq reads >5 on gene expression at each stage (iPSC, S1, S2).

2) Map ATAC-seq peaks (A: original peak calling) of 3 stages (iPSC, S1, S2) into locations of all genes (by finding the nearest promoter).

3) Use Venn diagrams to show the intersections of genes with stage-specific ATAC-seq peaks and gene that are stage-specifically expressed.  

###**Results**
1） Three tables of all the genes that reads >5.

*[iPS](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/Gene%20annotation/iPS_anno_1.csv)

*[S1](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/Gene%20annotation/S1_anno.csv)

*[S2](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/Gene%20annotation/S2_anno.csv)

2） Differential expression when comparing different stages. 

![genes in 3 stages](raw.githubusercontent.com/WPI-Wulab/ISO_seq/master/Studies/co_locate_images/vene_gene_3stage.jpeg)
![ss] ()https://raw.githubusercontent.com/zrs120100/images/master/test/S1_co_locate.png
3） The process of annotating peaks/regions is divided into two primary parts.  The first determines the distance to the nearest TSS and assigns the peak to that gene. 
 The second determines the genomic annotation of the region occupied by the center of the peak/region.

**Set different criterion: Distance to nearest RefSeq TSS <10000;**

![co_locate_iPS](raw.githubusercontent.com/zrs120100/images/master/test/S1_co_locate.png)

*[co_locate_S1](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/S1_co_locate_10000.png)

*[co_locate_S2](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/S2_co_locate_10000.png)

**Set different criterion: Distance to nearest RefSeq TSS <30000;**

*[co_locate_iPS](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/iPS_co_locate_30000.png)

*[co_locate_S1](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/S1_co_locate_30000.png)

*[co_locate_S2](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/S2_co_locate_30000.png)

**Set different criterion: Distance to nearest RefSeq TSS <10000;**

*[co_locate_iPS](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/iPS_co_locate_50000.png)

*[co_locate_S1](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/S1_co_locate_50000.png)

*[co_locate_S2](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/S2_co_locate_50000.png)

**Result from last week, without restrictions.**

*[co_locate_iPS](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/iPS_co_locate.png)

*[co_locate_S1](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/S1_co_locate.png)

*[co_locate_S2](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/S2_co_locate.png)

4） visualization in IGV

**Gene expression in 3 stages:**

*[NM_001402](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/igv_NM_001402.png)





