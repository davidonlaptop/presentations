
layout: true
---

## Mango: Massive data mining ANalysis of Genetic Observations

- TODO: fix front page
- David Lauzon
- ETS - DGA1031
- Montreal,QC, March 25th 2015
- Director: Prof. Alain April

---

## Plan
- Background and related work
- Problem definition 
- Research question & objectives
- Methodology
- Expected results
- Preliminary results
- Schedule
- References

---

## Background: Cell, DNA, Chromosome, Gene

![:svg](images/intro-cell-brain-eye-lungs.svg)

???

- Cell = Basic unit of life
- Organ = Each cell (brain, eye, lungs, ..) has the same DNA
- Chromosome = DNA is stored in chromosomes within the cell
- Gene = unit of genetic trait

---

## Background: Genome, Genomics
![:scale 90%](images/intro-genome.jpg)

???

- Genome = the 23 pairs of chromosomes (3 BILLIONS bp)
- Genomics = A discipline in genetics that study the genome

---

## Background: Amino acid (ACTG), BP
![:scale 100%](images/intro-acgt.jpg)

???

- DNA is chain of amino acids
- Amino acid = A,C,T,G
- BP = Since chromosomes comes in pair

---

## Background: Mutation ~ Variant (0.1%), SNP, Consequence
![:scale 95%](images/intro-mutation.jpg)

???

- Effect: A mutation may generate a different protein than expected (cell malfunction)
- Lots of data, but 99.9% the same

---

## Background: Allele, Genotype / Phenotype
![:scale 100%](images/intro-allele.jpg)

---

## Background: Cancer
![:scale 100%](images/intro-cancer.jpg)

---

## Genomic pipeline
![:svg](images/genomic.pipeline.svg)

---

## Main-stream technologies
![:svg](images/genomic.pipeline.mainstream.svg)

---

## Emerging technologies
![:svg](images/genomic.pipeline.bigdata.svg)

---

## Problem definition
- The most popular human genomic data analysis tool is plink (Harvard University)
- Large volume of data is slowing down the DNA variant discovery process
  - Some analysis task takes up to a **multiple days** to compute the results
- Most promising recent technology, ADAM (Berkeley University), uses Big Data techniques

---

## Research questions
- How can the performance of genomic analysis be improved?
  - What are the most problematic plink use cases today ?
  - What is the technological bottleneck ?
  - How can it be improved while retaining compatibility with existing software ?

---

## Objective of this research
- Propose a **scalable genomic analytics framework**, named MANGO, compatible with the ADAM format (Berkeley University).
- Identify the **missing data structures** in ADAM format to allow plink scalability;
- Identify the **Big Data techniques** that are required to improve the scalability of plink;

---

## Mango

![:svg](images/genomic.pipeline.mango.svg)

---

## Methodology - Planning (Basili Framework)

![:svg](images/basili.svg)

???

- **SURVEY** designed for bioinformaticians and geneticians to assess the most important features of plink software that slows down their DNA analysis process and their quality criteria for the adoption of a software replacement to plink.
- **PROBLEM**: Which analysis have poor scalability + What are the use expectations in ACCURACY & USABILITY from the users.
- **TECHNIQUES** includes data structures required to improve the scalability of plink software and end-user satisfaction 

---

## Methodology - Experimentation
- Tools used:
  - Apache **Spark**: Processing engine (Spark is the most active Big Data technology of 2014).
  - **MLlib**: machine learning library
  - **ADAM**: Genomics Formats
  - **Avocado**: DNA Variant Calling
  - **Scala**: programming language
  - **Docker**: infrastructure
  - **Parquet/Avro**: file format

---

## Expected results

- MANGO improves performs the selected analysis 5-10X faster than plink
  - MANGO results will be compared with Plink results
    - **Platform:** Amazon AWS (cloud computing)
    - **Dataset:** 5 open source genomes from the 1000 Genomes Project
    - **Nb of runs:** 5 runs on each dataset.
    - **Measure:** Job Turnaround time (ISO 25010) or _wall clock time_

---

## Preliminary results
- Collaboration with Berkeley University
  - Contributed patches to ADAM software
  - Contributed virtual infrastructure (Docker) for ADAM pipeline

- Collaboration with many health researchers
  - Genomic TM Simulator (Jewish General Hospital)
  - VariantMiner (Dr. Moreau, CHUSJ)
  - Dr. Hamet (CRCHUM)
  - Dr. Sinett (CHUSJ)
  - Pharmacogenomics Centre

---

## Originality of the work
- Use recent Big Data technologies to solve Genomics Analysis Performance Problems
  - Columnar file format
  - In-memory processing
  - Distributed computing
  - NoSQL datastore
  - Machine learning

- At the best of our knowledge, nobody has previously used these technologies to solve this use case

---

## Schedule

- (*2014 Fall*) DGA1005
- (*2015 Winter*) DGA1031
- (*2015 Summer*)
  - DGA1032
  - Survey
  - Identification of required scaling techniques 
- (*2015 Fall*) 
  - DGA1033
  - Case study 1
- (*2016 Winter*) MANGO prototype 1
- (*2016 Summer*) Case study 2
- (*2016 Fall*) 
  - MANGO prototype 2
  - Dissertation
- (*2017 Winter*) Dissertation
- (*2017 Summer*) Dissertation
- (*2017 Fall*) DGA1095 Defense

---

## References

- Zaharia, M., Chowdhury, M., Das, T., Dave, A., Ma, J., McCauley, M., ... & Stoica, I. (2012, April). Resilient distributed datasets: A fault-tolerant abstraction for in-memory cluster computing. _In Proceedings of the 9th USENIX conference on Networked Systems Design and Implementation_ (pp. 2-2). USENIX Association;
- Zaharia, M., Bolosky, W. J., Curtis, K., Fox, A., Patterson, D., Shenker, S., Stoica, I., Karp, R. M. & Sittler, T.  (1111). Faster and More Accurate Sequence Alignment with SNAP. In _Proceedings_;
- Massie, M., Nothaft, F., Hartl, C., Kozanitis, C., Schumacher, A., Joseph, A. D. & Patterson, D. A. (2013). ADAM: Genomics Formats and Processing Patterns for Cloud Scale Computing ( UCB/EECS-2013-207);
- Nothaft, F. A., Jin, P., Brown, B., of Electrical, D., Engineering, Computer & Science. avocado: A Variant Caller, Distributed. In _Proceedings_;
- Purcell, S., Neale, B., Todd-Brown, K., Thomas, L., Ferreira, M. A., Bender, D., ... & Sham, P. C. (2007). PLINK: a tool set for whole-genome association and population-based linkage analyses. _The American Journal of Human Genetics_, 81(3), 559-575.- Abran, A.  (2010). ISO 91261 : Analysis of Quality Models and Measures. IEEE.
- Jogalekar, P. & Woodside, M.  (2000). Evaluating the Scalability of Distributed and Systems. In . IEEE Transactions on parrallel and distributed systems, vol. 11, no. 6, june. 
