# OrganelleSRABuild
Pipeline to reconstruct chloroplast genome from the SRA database

OrganelleSRABuild is a pipeline to rebuild the chloroplast genomes
using a download-map-and-rebuild approach. 

The inputs are:
  * Chloroplast reference of a close related species (FASTA)
  * SRA accession (DbID) or short read dataset (FASTQ)
  * Species name (Name)

The tools that this program uses are:
  - Hisat2
  - Samtools
  - FreeBayes
  - Bgzip2
  - Tabix
  - Bedtools
  - Bcftools
  - Pilon

The steps performed by this tool are:
  1- Read mapping using HiSat2 to a chloroplast reference. Two possible inputs:
	a- Short read FASTQ dataset.
	b- SRA accession
  1- Sorting of the BAM file.
  1- Coverage estimation of the mapping.
  1- Variant calling.
  1- Consensus calling.
  1- Read remapping
  1- Polishing


