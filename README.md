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
 - They can be in the PATH;
 - You can specify a envirmental variable that points the tool to find the binaries.
 
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

Additionally for Pilon you will need to set up the PILON_RUN environmental variable
that defines where the file pilon.jar can be found.

```export PILON_RUN=/home/software/pilon/pilon.jar```

## Execution

Example 1: Download an SRA file and map with 1 thread

```OrganelleSRABuild -a SRR7692020 -o Nihet -r NibenCHL.fa```

Example 2: Download 3 SRA files and map with 8 threads

```OrganelleSRABuild -a SRR7692020,SRR7692023,SRR7451098 -o Nihet -r NibenCHL.fa -t 8```
