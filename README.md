# CobiontID

This repository provides an overview of the pipelines and tools developed to identify cobionts in the [Tree of Life Programme](https://www.sanger.ac.uk/programme/tree-of-life/). See https://cobiontid.github.io/ for more information!

## Software
### Standalone tools

| Tool | Description | Application | Language |
|--|--|--|--|
| [kmer-counter](https://github.com/CobiontID/kmer-counter) | Fast k-mer counter for large read sets | Get tetranucleotide counts | Rust |
| [unique-kmers](https://github.com/CobiontID/unique-kmer-counts) | Count distinct k-mers in sequences | Calculate k-mer diversity | Rust |
| [hexamer](https://github.com/richarddurbin/hexamer) | Detect likely coding regions | Estimate coding density | C |
| [fastk-medians](https://github.com/CobiontID/fastk-medians) | Calculate median number of times each large k-mer in a sequence occurs across the set (modified version of Profex from the original FASTK library) | Approximate k-mer coverage | C |

## Associated publications
*Phylogenomic analysis of Wolbachia genomes from the Darwin Tree of Life biodiversity genomics project* https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.3001972
