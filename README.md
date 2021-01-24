# TaskSolutions
some commonly used simple methods
To subset a bam file and convert it to fasta

# Sample command:

samtools view -b -h input.bam "10:18000-45500" > output.bam 
samtools fasta output.bam  > output.fasta


# Sample Rscript
#!/usr/bin/env Rscript
args = commandArgs(trailingOnly=TRUE)
# test if there is at least one argument: if not, return an error
if (length(args)==0) {
  stop("At least one argument must be supplied (input file).n", call.=FALSE)
} else if (length(args)==1) {
  # default output file
  args[2] = "out.txt"
}

### file "Mapability_100.txt"


BALL <- read.delim(args[1], header = TRUE)

### command line running: Rscript thiscript.R Mapability_100.txt
