# OrganelleSRABuild
Pipeline to reconstruct chloroplast genome from the SRA database

OrganelleSRABuild is a pipeline to rebuild the chloroplast genomes
using a download-map-and-rebuild approach. 

The inputs are:
  * Chloroplast reference of a close related species (FASTA)
  * SRA accession (DbID) or short read dataset (FASTQ)
  * Species name (Name)

## Installation

No installation is necessary. Just download the program with:

```git clone https://github.com/aubombarely/OrganelleSRABuild```

OrganelleSRABuils uses different tools (see the list below).
OrganelleSRABuildwill check that all the binaries and scripts are available. 
They can be available by two different methods: 
 1- They can be in the PATH;
 2- You can specify a envirmental variable that points the tool to find the binaries. 
    For example, if hisat2 is not in the PATH, you could use HISAT2_PATH to indicate
    OrganelleSRABuild where it can find hisat2-build and hisat2. 
    The available executable paths are: HISAT2_PATH,SAMTOOLS_PATH, FREEBAYES_PATH, 
    BGZIP2_PATH, TABIX_PATH, BCFTOOLS_PATH and BEDTOOLS_PATH. To set up the variable:

    ```export HISAT2_PATH=/home/software/hisat2_installation```

The tools that this program uses are:
  - Hisat2
  - Samtools
  - FreeBayes
  - Bgzip2
  - Tabix
  - Bedtools
  - Bcftools
  - Pilon




