# ncov-sim

During the analysis of SARS-CoV-2 genomes at the During the analysis of
SARS-CoV-2 genomes at the Ontario Institute for Cancer Research, human 
contamination within viral sequences was a high concern for
privacy reasons.  To combat this, a set of workflows was designed to filter
out human aligned reads providing SARS-CoV-2 sequences alone.  To test this,
whole genome data was downloaded from the Genome in a Bottle project for sample
`NA12878` (see Data Downloads section) along with viral genome sequencing data
for sample `NT04` from the Short Read Archive.  Selecting 10,000 reads from
the `NA12878` data and randomly inserting them into the `NT04`, a final set of
paired-end FASTQ files containing human spiked-in SARS-CoV-2 were created.

## Data Downloads
The data used in the generated reads can be found here:
```
ftp://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/data/NA12878/NIST_NA12878_HG001_HiSeq_300x/RMNISTHS_30xdownsample.bam
https://trace.ncbi.nlm.nih.gov/Traces/sra/?study=SRP253798
```

## References
* https://www.nature.com/articles/sdata201625


## License
MIT
