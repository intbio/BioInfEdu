# Cheat-sheet on processing NGS data
``` 
conda install fastqc
fastqc file.fastq
```
Download human genome from https://www.ncbi.nlm.nih.gov/genome/guide/human/

```
conda install bwa
bwa index -p hg19bwaidx -a bwtsw GRCh38_latest_genomic.fna
bwa aln -t 4 hg19bwaidx read1.fastq.gz > read1.bwa
bwa aln -t 4 hg19bwaidx read2.fastq.gz > read2.bwa
bwa sampe hg19bwaidx read1.bwa read2.bwa read1.fastq.gz read2.fastq.gz > aligned.sam
conda install samtools
# samtools view -Sb aligned.sam > aligned.bam
samtools sort aligned.sam > aligned.bam
samtools index aligned.bam aligned.bam.bai
```
Now should be viewable by IGV
