#Research Report for Co-locate RNA transcripts 

###**Description**: 

The report is about co-locate RNA transcripts identified by ISO-seq of iPSC, 
S1 and S2 cells with stage-specific open chromatin domains identified by ATAC-Seq based on 
gene level.

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

1） Differential expression when comparing different stages (genes with more than 5 reads (6 or more)). 
**Refseq**
 
![genes in 3 stages](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/vene_gene_3stage.jpeg)

**Gene**

![3 stages expressed genes](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/3%20stages%20expressed%20genes.png)

There are 750 genes common expressed. In stage iPS and S1, there are more than 1426 genes
expressed in both stages.
In stage S1, it has maximum quantity(1298) specific genes.
2） Pick some highly expressed genes to show visualization. 

**EEF1A1**

![EEF1A1](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/EEF1A1.png)

**HMGA1**

![HMGA1](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/HMGA1.png)

**ACTB**

![ACTB](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/ACTB.png)

3) ATAC-Seq and Iso-Seq co-locate results in 3 stages.

**First, we use Refseq ID to do co-locate, there are no more than 20% Iso-Seq colocate with ATAC-Seq.** 

**iPS stage**

![co_locate_iPS](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/iPS_co_locate.png)

**S1  stage** 

 ![co_locate_S1](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/S1_co_locate.png)
 
 **S2 stage**
 
 ![co_locate_S2](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/S2_co_locate.png)

**On gene level, many different Refseq IDs correspoding to one gene ID because genes have transcript variants(ex. NM_199185, NM_002520, NM_001037738 correspoding to NPM1). We need to covert Refseq ID to Gene ID by *UniProt*.** 

**iPS stage**

Overall, 1880 genes that were expressed at significantly higher levels in stage S1 were associated with ATAC-Seq, which accounted for  85% of expressed genes.

![co_locate_iPS](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS.png)

**Different ways define ATAC-seq: Given a distance to TSS**

Less than 100bp
 
![iPS<100](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS/iPS_100.png)

Less than 500bp

![iPS<500](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS/iPS_500.png)

Less than 1000bp

![iPS<1000](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS/iPS_1000.png)

**iPS VS S1, Common ATAC-peaks expressed genes**

![iPS/S1 COMMON EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS_S1/iPS/common.png)

**Common ATAC-peaks expressed genes with common expressed genes in iPS**

![iPS common expressed](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS_S1/iPS/common_common.png)

**iPS VS S1, stage specific ATAC-peaks expressed genes**

![iPS specific EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS_S1/iPS/iPS.png)

**stage specific ATAC-peaks expressed genes co-locate with specific expressed genes in iPS**

![iPS specific EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS_S1/iPS/iPS_spe.png)

**iPS VS S2, Common ATAC-peaks expressed genes**

![iPS/S2 COMMON EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS_S2/iPS/common.png)

**iPS VS S2, stage specific ATAC-peaks expressed genes**

![iPS specific EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS_S2/iPS/iPS.png)

**S1  stage**

Overall, 2808 genes that were expressed at significantly higher levels in stage S1 were associated with ATAC-Seq, which accounted for  84% of expressed genes.

 ![co_locate_S1](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/S1.png)
 
 **Different ways define ATAC-seq: Given a distance to TSS**
 
 Less than 100bp
  
 ![S1<100](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/S1/100.png)
 
 Less than 500bp
 
 ![S1<500](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/S1/500.png)
 
 Less than 1000bp
 
 ![S1<1000](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/S1/1000.png)
 
 **iPS VS S1, Common ATAC-peaks expressed genes**
 
 ![iPS/S1 COMMON EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS_S1/S1/common.png)
 
 **iPS VS S1, stage specific ATAC-peaks expressed genes**
 
 ![S1 specific EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS_S1/S1/S1.png)
 
 
 **S1 VS S2, Common ATAC-peaks expressed genes**
 
 ![S1/S2 COMMON EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/S1_S2/S1/common.png)
 
 **S1 VS S2, stage specific ATAC-peaks expressed genes**
 
 ![S1 specific EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/S1_S2/S1/S1.png)
 
 **S2 stage**
 
Overall, 1349 genes that were expressed at significantly higher levels in stage S1 were associated with ATAC-Seq, which accounted for  81% of expressed genes.
 
 ![co_locate_S2](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/S2.png)
 
**Different ways define ATAC-seq: Given a distance to TSS**
 
 Less than 100bp
  
 ![S2<100](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/S2/100.png)
 
 Less than 500bp
 
 ![S2<500](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/S2/500.png)
 
 Less than 1000bp
 
 ![S2<1000](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/S2/1000.png)
 
 **iPS VS S2, Common ATAC-peaks expressed genes**
 
 ![iPS/S2 COMMON EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS_S2/S2/common.png)
 
 **iPS VS S2, stage specific ATAC-peaks expressed genes**
 
 ![S2 specific EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/iPS_S2/S2/S2.png)
 
 **S1 VS S2, Common ATAC-peaks expressed genes**
 
 ![S1/S2 COMMON EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/blob/master/Studies/co_locate_images/gene%20level/S1_S2/S2/common.png)
 
 **S1 VS S2, stage specific ATAC-peaks expressed genes**
 
 ![S2 specific EXPRESSED](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/co_locate_images/gene%20level/S1_S2/S2/S2.png)
 
These results suggest that open chromatin may be a good predictor of gene activation in 3 stages. Although the number of genes changing in different stages, the percent of it doesn't show obvious variation. Perhaps there is no inherent differences in gene regulation in
these three stages. Even though setting lower criterion of distance to TSS, half of the genes in different stages still can be predicted by ATAC-seq.

Furthermore, there were many more genes with ATAC-seq peaks that were not expressed in Iso-Seq among 3 stages. Only 8%, 14% and 7% ATAC-seq peaks mapped to differentially expressed genes. 

Most expressed genes in three stages co-locate with genes related to common ATAC-peaks. This proves that there is no inherent differences in gene regulation process.

##Coloate based on location
Tool: bedtools

###-f 
At least one based is overlapped between feature A and B is regared as one overlap.
![iPS](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/Co-locate%20based%20for%20bedtools/-f/Integration%20of%20ATAC-seq%20and%20ISO-seq%20in%20iPS.jpeg)

![S1](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/Co-locate%20based%20for%20bedtools/-f/Integration%20of%20ATAC-seq%20and%20ISO-seq%20in%20S1.jpeg)

![S2](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/Co-locate%20based%20for%20bedtools/-f/Integration%20of%20ATAC-seq%20and%20ISO-seq%20in%20S2.jpeg)

### -f 0.25
At least 25% regions is overlapped between feature A and B is regared as one overlap.
![iPS](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/Co-locate%20based%20for%20bedtools/-f%200.25/Integration%20of%20ATAC-seq%20and%20ISO-seq%20in%20iPS%20with%20-f%200.25.jpeg)

![S1](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/Co-locate%20based%20for%20bedtools/-f%200.25/Integration%20of%20ATAC-seq%20and%20ISO-seq%20in%20S1%20with%20-f%200.25.jpeg)

![S2](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/Co-locate%20based%20for%20bedtools/-f%200.25/Integration%20of%20ATAC-seq%20and%20ISO-seq%20in%20S2%20with%20-f%200.25.jpeg)

###-f 0.50
At least 50% regions is overlapped between feature A and B is regared as one overlap.
![iPS](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/Co-locate%20based%20for%20bedtools/-f%200.5/Integration%20of%20ATAC-seq%20and%20ISO-seq%20in%20iPS%20with%20-f%200.5.jpeg)

![S1](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/Co-locate%20based%20for%20bedtools/-f%200.5/Integration%20of%20ATAC-seq%20and%20ISO-seq%20in%20S1%20with%20-f%200.5.jpeg)

![S2](https://github.com/WPI-Wulab/ISO_seq/raw/master/Studies/Co-locate%20based%20for%20bedtools/-f%200.5/Integration%20of%20ATAC-seq%20and%20ISO-seq%20in%20S2%20with%20-f%200.5.jpeg)

##Gene annotation for all stages 
Tool: Homer  




