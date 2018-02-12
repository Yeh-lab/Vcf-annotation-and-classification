# Vcf-annotation-and-classification
Vcf files annotation and classification 

1.	Pathogenic vcf file

   a.	Extract ‘CLINSIG=pathogenic|CLINSIG=probable-pathogenic’ SNV.

   b.	Remove SNV with ‘10X_HOMOPOLYMER_UNPHASED_INSERTION|10X_RESCUED_MOLECULE_HIGH_DIVERSITY’, this should be false positive (https://support.10xgenomics.com/genome-exome/software/pipelines/latest/output/vcf).

2.	Germline vcf file

   a.	Extract each SNV with frequency of ExAC_ALL (>0) or esp6500 (>0) or 1000g (>0)

   b.	Remove  SNV with ‘10X_HOMOPOLYMER_UNPHASED_INSERTION|10X_RESCUED_MOLECULE_HIGH_DIVERSITY’, this should be false positive.

3.	Somatic vcf file 

   a.	Remove Pathogenic SNV, Germline and SNVs ‘10X_HOMOPOLYMER_UNPHASED_INSERTION|10X_RESCUED_MOLECULE_HIGH_DIVERSITY’. 

   b.	Remove SNVs in UTR3|UTR5|downstream|intergenic|intronic|ncRNA|upstream, except for TERT, SDHD and NFKBIE (upstream). 
