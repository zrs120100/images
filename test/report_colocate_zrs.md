#Research Report for Co-locate RNA transcripts 

###**Description**: 

The report is about co-locate RNA transcripts identified by ISO-seq of iPSC, 
S1 and S2 cells with stage-specific open chromatin domains identified by ATAC-Seq.

###**Steps**:

1) Get all the genes that ISO-seq reads >5 on gene expression at each stage (iPSC, S1, S2) by using Homer.
Draw the venn diagram to show the number of common expression genes and number of specific expression genes.

2) Map ATAC-seq peaks (A: original peak calling) of 3 stages (iPSC, S1, S2) into locations of all genes
 by using Homer(finding the nearest promoter). 

3) On gene level, find out the genes that are differentially expressed in the same stage of Iso-Seq and ATAC-Seq.
Use Venn diagrams to show the intersections in 3 stages.  

4) Use IGV to show some specific genes that are higher expressed in 3 stages.

**For annotation, the GTF file is HG19.**

###**Results**
1） Three tables of all the genes that reads >5.

*[iPS](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/Gene%20annotation/iPS_anno_1.csv)

*[S1](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/Gene%20annotation/S1_anno.csv)

*[S2](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/Gene%20annotation/S2_anno.csv)

2） Differential expression when comparing different stages. 

![genes in 3 stages](https://raw.githubusercontent.com/WPI-Wulab/ISO_seq/master/Studies/co_locate_images/vene_gene_3stage.jpeg?token=AgAV6mqnowlCOTpmSQ7HZep1XGREfQlXks5ai5h4wA%3D%3D)

There are 2487 genes common expressed. In stage iPS and S1, there are more than 4500 genes
expressed in both stages.
In stage S1, it has maximum quantity specific genes.

3） 
![co_locate_iPS](https://raw.githubusercontent.com/WPI-Wulab/ISO_seq/master/Studies/co_locate_images/iPS_co_locate.png?token=AgAV6g9gGceADsHAP2WMvVYjA0C979vpks5ai6OLwA%3D%3D)
 
 ![co_locate_S1](https://raw.githubusercontent.com/WPI-Wulab/ISO_seq/master/Studies/co_locate_images/S1_co_locate.png?token=AgAV6lyjgyr_TrYRpKFUv1SE8XLyHYVtks5ai6OfwA%3D%3D)
 
 ![co_locate_S2](https://raw.githubusercontent.com/WPI-Wulab/ISO_seq/master/Studies/co_locate_images/S2_co_locate.png?token=AgAV6ilPe5xIQDcGBOmux4I6V8RVLZlzks5ai6O8wA%3D%3D)

There are 



4） visualization in IGV

**Gene expression in 3 stages:**

*[NM_001402](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/igv_NM_001402.png)





