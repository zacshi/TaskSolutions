# TaskSolutions
some commonly used simple methods
To subset a bam file and convert it to fasta

#Sample command:
samtools view -b input.bam "10:18000-45500" > output.bam 
samtools fasta output.bam  > output.fasta
