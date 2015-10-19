# README #

FindCleavageSite.py takes as input sorted BAM files, generated by bwa.

## Current CIRCLE-seq workflow##

This is a repository for programs associated with analysis of Comprehensive In vitro Reporting of CLeavage Effects by Sequencing (CIRCLE-seq).

1. The first step is to map the reads to the human reference genome using bwa.
2. The second step is to sort the reads by read name to group paired end reads.
3. The final step is to run FindCleavageSites-Circular.py to identify CIRCLE-seq Cas9 off-target cleavage sites.

    
```


python /data/joung/bitbucket/invitro-guide-seq/FindCleavageSites.py --reads 3 \ 
--bam /data/joung/sequencing_fastq/150529_M01326_0203_000000000-AEENP/BAM/SQT01_S1.bam \
--ref /data/joung/genomes/Homo_sapiens_assembly19.fasta --targetsite GGGTGGGGGGAGTTTGCTCCNGG > VEGFA_1_ivgs.bed
```