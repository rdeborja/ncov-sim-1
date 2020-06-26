# ncov-sim

To allow public sharing of SARS-CoV-2 sequencing data, care must be made to
filter out any background human sequencing data. To combat this, a set of 
workflows was designed to filter out human aligned reads providing SARS-CoV-2 
sequences alone.  To test this, whole genome data was downloaded from the 
Genome in a Bottle project for sample `NA12878` (see Data Downloads section) 
along with viral genome sequencing data for sample `NT04` from the Short Read 
Archive.  Selecting 10,000 reads from the `NA12878` data and randomly inserting
 them into the `NT04`, a final set of paired-end FASTQ files containing human 
spiked-in SARS-CoV-2 were created.


## Data Downloads
The data used in the generated reads can be found here:
```
ftp://ftp-trace.ncbi.nlm.nih.gov/ReferenceSamples/giab/data/NA12878/NIST_NA12878_HG001_HiSeq_300x/RMNISTHS_30xdownsample.bam
https://trace.ncbi.nlm.nih.gov/Traces/sra/?study=SRP253798
```


## Generated Spike-In Reads
Pre-generated data is provided in the `data` directory and includes SARS-CoV-2 reads from host `NT04` with `NA12878` human host reads.  Aligment were filtered from the `NA12878` BAM file for mapping quality > 30.  Aligments were name sorted using `samtools sort` and limited to the first 5000 read pairs.  The alignments were converted to FASTQ files using `samtools fastq` and added to the SARS-CoV-2 reads using the `spikein_reads.py` script.


## References
* https://www.nature.com/articles/sdata201625
* http://www.htslib.org


## License
MIT
