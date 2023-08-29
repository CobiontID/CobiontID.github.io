---
title: CobiontID overview
layout: page
show_sidebar: false
menubar: docs_menu

---
# Identifying cobionts and contaminants

Disentangling sequences from different sources can be both interesting and challenging. It can reveal interactions between organisms and their genomes through time (considering extant associations and molecular fossils). In some cases, the aim may simply be to remove contamination that has found its way into a sample. However, determining where a sequence came from is not always straightforward - especially when exploring less well sampled parts of the tree of life, where few close relatives have been sequenced.

On these pages, you will find some examples showing how we are tackling this issue in the <a href="https://www.sanger.ac.uk/programme/tree-of-life/">Tree of Life</a> programme. Our approach, which is tailored for HiFi data, combines grouping sequences from the same source with finding reliable taxonomic hints. This allows us to reduce reliance on databases, which can be incomplete and contain mislabelled sequences.

<img src="https://user-images.githubusercontent.com/10507101/218132172-1ae5b98c-2770-46c4-9740-37b30ec1b7d5.png" width=300>


## The CobiontID approach

The **CobiontID** process has two parts: First, **Marker scan** provides taxonomic information. HMM profiles of marker genes, such as rRNAs, which are well-sampled and conserved, are useful to classify sequences from genomes that are otherwise too diverged from their closest sequenced relative. We can therefore gauge which species are present in a given sample, and construct streamlined databases for read classification. Second, a combination of assembly, read mapping and **compositional clustering** allows the sequences to be assigned to groups that can be tagged with this taxonomic information.

### What kind of information does CobiontID provide?

See [here] for an illustration of the outputs the tools presented here provide, and how to interpret them. If you have ever looked at the "Cobionts" section of a page on [Tree of Life QC](https://tolqc.cog.sanger.ac.uk/) and wondered how to read the tables and plots, your questions will hopefully be answered here.

[here]: examples.html

### Software used in the pipelines
#### Standalone tools

| Tool | Description | Application | Language |
|--|--|--|--|
| [kmer-counter](https://github.com/CobiontID/kmer-counter) | Fast k-mer counter for large read sets | Get tetranucleotide counts | Rust |
| [unique-kmers](https://github.com/CobiontID/unique-kmer-counts) | Count distinct k-mers in sequences | Calculate k-mer diversity | Rust |
| [hexamer](https://github.com/richarddurbin/hexamer) | Detect likely coding regions | Estimate coding density | C |
| [fastk-medians](https://github.com/CobiontID/fastk-medians) | Calculate median number of times each large k-mer in a sequence occurs across the set (modified version of Profex from the original FASTK library) | Approximate k-mer coverage | C |

#### Workflows
| Workflow | Description |
|--|--|
|[MarkerScan](https://github.com/CobiontID/MarkerScan) | Determine taxonomic composition of an assembly; separate and assemble individual components |
|[read VAE](https://github.com/CobiontID/read_VAE/) | Generate annotated 2D visualisations for long reads; interactively explore and select data for downstream analyses |

## Additional information
![image](https://user-images.githubusercontent.com/10507101/218133727-b8cd1860-d33e-4955-8d2e-473d770def84.png) [GitHub](https://github.com/CobiontID/)
- [Slides](https://drive.google.com/file/d/1ghtPRkdNZRLfDH-pTluUJ2Xq1IpKRaht/view) from talk on CobiontID at PopGroup55 (2022)
- [Flash presentation](https://twitter.com/cc7740/status/1479071728697548807) accompanying PopGroup talk
