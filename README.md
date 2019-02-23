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
  1. Read mapping using HiSat2 to a chloroplast reference. Two possible inputs:
	a- Short read FASTQ dataset.
	b- SRA accession
  2. Sorting of the BAM file.
  3. Coverage estimation of the mapping.
  4. Variant calling.
  5. Consensus calling.
  6. Read remapping
  7. Polishing


