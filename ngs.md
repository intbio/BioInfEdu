# Cheat-sheet on processing NGS data
``` 
conda install fastqc
fastqc file.fastq
```
Download human genome from https://www.ncbi.nlm.nih.gov/genome/guide/human/

```
conda install bwa
bwa index -p hg19bwaidx -a bwtsw GRCh38_latest_genomic.fna
```
