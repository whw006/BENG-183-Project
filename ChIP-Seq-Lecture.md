# ChIP-Seq

1. [Introduction](#intro)
2. [Methods](#methods)
3. [Analysis Pipeline](#analysis)
4. [References](#analysis)


## Introduction <a name="intro"></a>

### What is ChIP-Seq?
**Ch**romatin **I**mmuno**p**recipitation **Seq**uencing is a procedure that is used to determine the binding sites of DNA transciption factors using immunoprecipitation and high throughput sequencing.

#### What is is used for?
Identifying genome-wide DNA binding sites for transcription factors. Allows for easy identification of binding sites of a specific protein target. This requires a protein specific antigen for immunoprecipitation of target the target protein.

#### What are the advantages over existing technology?

This technology was developed as a better alternative to Chip  captures DNA targets for transcription factors or histone modifications across the entire genome and defines transcription factor binding sites.


## Methods<a name="methods"></a>

In order to conduct ChIP-seq it is necissary to first identify the target transcription factor or histone modification you want to study. Once the protein is identified, an antigen specific to the  protein needs to be designed for the immunoprecipitation step. This is crucial for isolating DNA attached to the protein since the antigen is able to bind to the protein and is then easily isolated. 

#### Protocol Overview: 
1. ChIP-Sequencing is initialized with the crosslinking of proteins to the DNA using formaldehyde.
2. The nuclei are isolated and lysed then the chromatin is sonicated for fragmentation.
3. Target DNA is isolated during the  immunoprecipitate step. 
Antibodies specific to target protein are attached and used to isolate sections of DNA that the protein is bound to.
4. ChIP DNA is purified by reversing the crosslinking of proteins and the DNA is prepped for high-throughput sequencing.

A full lab protocol for ChIP-seq can be found here: https://currentprotocols.onlinelibrary.wiley.com/doi/full/10.1002/0471142727.mb2119s91

## Analysis<a name = "analysis"></a>



1. Match output file to reference genome
   - Individual reads from sequencing are presented in FASTQ format
   - Reads are mapped to reference genome
   
2. Determine significance of reads locations based on quantity and uniqueness of each read.
   - Highly significant locations will have high quantities of reads.
   - Need to account for reads mapped to more than one location 
   - Eliminate low quality reads

3. Data Visualization
   - Good data visualization is vital for making inferences about data
   - Easy way is to use a genome browser
   - GIVE allows easy lookup and code generation for ChIP-Seq data

4. Interpreting Data
   - Identify potential binding motif of Transcription Factor
     - Motif: Common binding sequence
     - Importance of each nucleotide is denoted by the size of each letter
   - Identify evolutionary dynamics as done in this paper by Dominic Schmidt
https://www.ncbi.nlm.nih.gov/pubmed/20378774




## References<a name = "references"></a>

[1] Bailey, Timothy et al. “Practical guidelines for the comprehensive analysis of ChIP-seq data” PLoS computational biology vol. 9,11 (2013): e1003326.
 
Link: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3828144
 
[2] “Chromatin Immunoprecipitation Sequencing (ChIP-Seq).” Sequencing Technology | Sequencing by Synthesis, Illumina, www.illumina.com/techniques/sequencing/dna-sequencing/chip-seq.html.
 
Link: www.illumina.com/techniques/sequencing/dna-sequencing/chip-seq.html
 
[3] Raha, Debasish, et al. “ChIP-Seq: A Method for Global Identification of Regulatory Elements in the Genome.” Current Protocols in Molecular Biology, vol. 91, no. 1, 15 July 2010, doi:10.1002/0471142727.mb2119s91.
 
Link: https://currentprotocols.onlinelibrary.wiley.com/doi/full/10.1002/0471142727.mb2119s91
 
[4] Schmidt, Dominic et al. “Five-vertebrate ChIP-seq reveals the evolutionary dynamics of transcription factor binding” Science (New York, N.Y.) vol. 328,5981 (2010): 1036-40.

Link: https://www.ncbi.nlm.nih.gov/pubmed/20378774
 
[5] Zhong. “ChIP Sequencing” Lecture, 16 October 2018.
 
Link: https://docs.google.com/presentation/d/1Va34FmS3-DqZXPqmbybBgL1qgNaUwcGcm86wXHkKrlI/edit#slide=id.p16
