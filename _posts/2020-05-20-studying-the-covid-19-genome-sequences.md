---
date: 2020-05-20 13:05:07
layout: post
title: "Studying the COVID-19 genome sequences"
subtitle: 
description: Exploratory Data Analysis on COVID-19 and other coronavirade family's viruses' genome sequences
image: https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/900px-Difference_DNA_RNA-EN.svg.png
optimized_image: https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/600px-Difference_DNA_RNA-EN.svg.png
category: data analysis
tags:
- DataAnalysis
- COVID-19
- DataVisualization
- GenomeSequenceAnalysis
- PhylogeneticTree
author: Aman Singh
paginate: false
---

This [notebook](https://www.kaggle.com/amansingh29/unwrapping-the-covid-19-genomes/) is an attempt to answering some of the questions of bio-informatics in regards to the recent panademic outbreak of Corona virus, from a non-medical background person's perspective. Every analysis presented here is based on the stuff I learnt and understood (or felt that I actually understood) about the genomes from the internet.

# Some Context
**[Ques.] What is Genome?**<br>
[Genomes](https://en.wikipedia.org/wiki/Genome) are considered to be genetic material of any organism. It consists of [DNA](https://en.wikipedia.org/wiki/DNA)(or [RNA](https://en.wikipedia.org/wiki/RNA)) which in turn can be considered as the blueprints of any organisms' origin.
<img src="https://www.genome.gov/sites/default/files/tg/en/illustration/acgt.jpg" width=550 height=400>

**[Ques.] How to study Genomes?**<br>
A genome consists of a sequence of [nucleotides](https://en.wikipedia.org/wiki/Nucleotide) that together make up all the [chromosomes](https://en.wikipedia.org/wiki/Chromosome) of any organism. These nucleotides are the basic building blocks of DNA and RNA. A DNA genome has 4 types of base nucleotides -<br> `Adenine` also represented as `A`,<br>`Thymine` represented as `T`,<br>`Guanine` represented as `G` and<br>`Cytosine` represented as `C`.<br> In RNA genome, the `Thymine` nucleotide is replaced with what is known as `Uracil` represented as `U`.<br> In short, any genome sequence is basically a combination of all these nucleotide in smoe order.

**[Ques.] Can one find a cure for [COVID-19](https://en.wikipedia.org/wiki/Coronavirus_disease_2019) by just studying the genomes?**<br>
**Not sure**, as the [molecular biology](https://en.wikipedia.org/wiki/Molecular_biology) has not really been my field of study (*never liked Biology tbh*) but also because its a very vast subject where to confirm on a single hypothesis also takes months/years of evaluation and testing. Having said that, the whole purpose of this analysis is to help the ones who actually understand molecular biology get some data-driven insights to be able to preapare a RNA vaccine at the earliest.
<img src="https://images.theconversation.com/files/324780/original/file-20200402-23151-18gxxtu.png" width=500 height=500>

lets have a look at a snippet of one of the genomes,
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/genome-seq.JPG">

having a huge sequence and with everyting in single color could be difficult to read. So let's color-code these nucleotides in the sequences and have them represented as they are normally written.
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/covid19-genome-seq.JPG">

# Comparison of composition of genomes
Comparing the genomic composition, helps Vaccinologist do [reverse vaccinology](https://en.wikipedia.org/wiki/Reverse_vaccinology) to discover candidate [antigents](https://en.wikipedia.org/wiki/Antigen) for vaccine development by analyzing the genome of a pathogen or a family of pathogens.

For the comparison of composition of these genomes, I'll be looking at the<br>
- Oligonucleotide composition<br>
- GC content

### 1. Oligonucleotide composition:
[Oligonucleotides](https://en.wikipedia.org/wiki/Oligonucleotide) are DNA or RNA molecules made up of a sequence of nucleotides. The length of the oligonucleotide is represented as "[k-mer](https://en.wikipedia.org/wiki/K-mer)" ($k$ being the number of nucleotides in one oligonulceotide). In this analysis, I'll be looking at the **3-mers** (or **trinucleotides**) and **4-mer** (or **tetranucleotides**) compositions against their normalized frquency of occurrences.
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/3mer.png">

Now lets have a look at the tetramer composition of these genomes
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/4mer.png">

Well that's alot to put in one plot, but the good thing with plotly is that you can always turn off a few legends to compare the values just among the selected few.

For a moment, lets just look at the tetranucleotide composition of all the "corona-virus infected species".
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/4mercov.png">

### 2. GC Content:
**[GC content](https://en.wikipedia.org/wiki/GC-content)** (or **Guanine-Cytosine content**) is the percentage of nucleotides bases in a DNA/RNA molecule that are either guanine (G) or cytosine (C). GC content is always expressed as a percentage value and is supposed to remaine the same among genomes of same specie.

$$\frac{G + C}{A + C + G + T} \times 100\ \%$$
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/gc.png">

# Proteins & Amino Acids
The most commonly occuring amino acids are abbreviated by using 20 letters from the english alphabet (all letters except for B,J,O,U,X and Z). The protein strings are constructed from these 20 alphabets as symbols. Henceforth, a Protein Sequence can also be incorporated using the nucleotide sequences.

<img src="https://1.bp.blogspot.com/-QpZ1VXFbJhE/V4d5EjT3FYI/AAAAAAAADvk/UGZK71q3KV4AwrOfR_bdEk2FnC93Cb-JwCLcB/s1600/codon.png">

The DNA codon table on [wiki](https://en.wikipedia.org/wiki/DNA_codon_table) dictates the details regarding the encoding of specific codons into amino acids alphabets.

lets have a look at the protein sequences of a few of these genome before we go for a comparative analysis
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/malaria_pro.JPG">

<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/cov_pro.JPG">

### 1. Protein Strands by genome
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/proteins.png">

### 2. Amino Acids Distribution
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/amino.png">

### 3. Finding the ORFs (Open Reading Frames)
The stretch of codons from start-codon (ATG) to stop-codon (TAA/TAG/TGA) is called [Open Reading Frame (ORF)](https://en.wikipedia.org/wiki/Open_reading_frame)

the highlighted sequences below represent the ORFs

<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/orf.JPG">

### 4. Comparative Summary of Protein Sequences
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/pro_summary.png">

# Sequence Alignement
The sequence alignment is a way of arranging the sequences of DNA/RNA or protein to identify regions of similarity that may be a consequence of functional, structural, or evolutionary relationships between the sequences. These in turn help in identifying the sequence similarities and developing homology models of protein structures. Alignments are often assumed to reflect a degree of evolutionary change between sequences descended from a common ancestor.

as the genomes sequences are too big in length, lets align and have a look at just the first few nucleodtides in the sequences
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/seq.JPG">

let us also have a look at the first few aligned protein sequences of these genomes
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/pro_seq.JPG">

# Pairwise Sequence Alignment
earlier we had aligned every sequence based on the [Clustal](https://en.wikipedia.org/wiki/Clustal) algorithm, now let's align every other genome with the covid19 genomes.
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/align.JPG">

# Genome Sequence Similarity
**using Clustal algorithm**<br>

for establishing the similarity among genomes, we'll be changing the scoring parameter<br>
for every match there will be a +1 point<br>
for every mismatch there will be a -1 point<br>
for every open gap there will be a -0.5 points<br>
for every extended gap there will be a -0.1 point<br>

```
Similarity scores between

COVID-19 & SARS genome sequences:	 20885.00000000038 (69.84%)
COVID-19 & MERS genome sequences:	 15122.599999998136 (50.57%)
COVID-19 & Civet_SL_CoV genome sequences:	 20616.90000000066 (68.95%)
COVID-19 & Bat_SL_CoV genome sequences:	 20706.000000000255 (69.24%)
COVID-19 & Ebola genome sequences:	 10233.39999999796 (34.22%)
COVID-19 & Camel_CoV genome sequences:	 15134.599999998123 (50.61%)
COVID-19 & Malaria genome sequences:	 8.800000000105774 (0.03%)
COVID-19 & HIV genome sequences:	 5962.5999999990445 (19.94%)
COVID-19 & Hedgehog_CoV genome sequences:	 15227.29999999811 (50.92%)
```

# Generating a Phylogenetic Tree
A [Phylogenetic Tree](https://en.wikipedia.org/wiki/Phylogenetic_tree) is the tree of evolutionary relationship among various species based on their genetic characteristics.
### UPGMA (Unweighted Pair Group Method with Arithmetic mean) algorithm
This is where you can learn more about it [wiki](https://en.wikipedia.org/wiki/UPGMA)<br>
[NOTE] unlike the above sequence similarity, here only the mismatch cases are scored using the aligner and no scoring is done for gaps and extended gaps.

<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/phylo1.JPG">
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/phylo1c.JPG">

# Clustering all COVID-19 patients' genomes
using the UPGMA algorithm

<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/phylo2.JPG">
<img src="https://raw.githubusercontent.com/amansingh9097/amansingh9097.github.io/master/assets/img/uploads/covid19-genomes/phylo2c.JPG">

# Conclusions
- Based on the oligonucleotide compositions, all the genomes from coronaviridae family show similar composition (trinucleotide and tetranucleotide composition)<br>
- Based on GC content, the composition of Hedgehog infected Corona virus is closely similar to COVID-19 genome's GC content.<br>
- Judging by the number of protein strands, the count in COVID19's genome is very close to those found in Bat infected with SARS like corona virus.<br>
- If you filter down some of the categories in the plotly-plot of distribution of amino acids, you'll see the percentage of amino acids in COVID-19's genome closely match to those of MERS, Civet infected with SARS like CoV, Camel with alpha CoV and Malaria except for some and low high contents among L (Leucine), P (Proline) and T (Threonine) amino acids.<br>
- Checking by the generated Phylogenetic tree, the genomes of COVID-19 and malaria virus show the maximum similarity. Perhaps this also explains why there's a lot of buzz on the news and internet about trying Hydroxycholorquine and anti-retroviral drugs which happen to be the medicines for malaria and HIV viruses, respectively.<br>
- Of all the genomes of COVID-19 infected patients avaialable on Kaggle, some patients show similar traits when clustered based on their genome sequence similarity.I really don't know how helpful this would be but if something works or had worked for a patient, then same should also work for patients in the same cluster.<br>

--- 

If you liked this project, please consider buying me a coffee<br>
<style>.bmc-button img{height: 34px !important;width: 35px !important;margin-bottom: 1px !important;box-shadow: none !important;border: none !important;vertical-align: middle !important;}.bmc-button{padding: 7px 10px 7px 10px !important;line-height: 35px !important;height:51px !important;min-width:217px !important;text-decoration: none !important;display:inline-flex !important;color:#ffffff !important;background-color:#FF813F !important;border-radius: 5px !important;border: 1px solid transparent !important;padding: 7px 10px 7px 10px !important;font-size: 28px !important;letter-spacing:0.6px !important;box-shadow: 0px 1px 2px rgba(190, 190, 190, 0.5) !important;-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;margin: 0 auto !important;font-family:'Cookie', cursive !important;-webkit-box-sizing: border-box !important;box-sizing: border-box !important;-o-transition: 0.3s all linear !important;-webkit-transition: 0.3s all linear !important;-moz-transition: 0.3s all linear !important;-ms-transition: 0.3s all linear !important;transition: 0.3s all linear !important;}.bmc-button:hover, .bmc-button:active, .bmc-button:focus {-webkit-box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;text-decoration: none !important;box-shadow: 0px 1px 2px 2px rgba(190, 190, 190, 0.5) !important;opacity: 0.85 !important;color:#ffffff !important;}</style><link href="https://fonts.googleapis.com/css?family=Cookie" rel="stylesheet"><a class="bmc-button" target="_blank" href="https://www.buymeacoffee.com/amansingh"><img src="https://cdn.buymeacoffee.com/buttons/bmc-new-btn-logo.svg" alt="Buy me a coffee"><span style="margin-left:15px;font-size:28px !important;">Buy me a coffee</span></a>