# Genomics Pipeline

1. Pre-processing
  - Raw reads
  - Align to reference genome
  - Sort by reference order
  - Mark duplicates
  - Indel realignment
  - Base quality score recalibration (BQSR)

2. Variant Discovery
  - Variant calling (per sample)
  - Joint genotyping (per cohort)
  - Variant filtering (per cohort)

3. Preliminary analysis
  - Genotype phasing
  - Genotype imputation
  - Genotype filtering
  - Functional annotation
  - Variant evaluation

4. Genome-wide association studies (GWAS) 
  - Variants management
  - Summary stats
  - Population stratification
  - Permutations
  - Associations (family, proxy)
  - Haplotype imputation
  - Copy Number Variations
  - ...

???

4 main activities
