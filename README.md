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

### Dashboard
A demo of the interactive dashboard to explore read sets is available [here](https://huggingface.co/spaces/cc7740/read_VAE). You can also try running the demo on [Gitpod](https://gitpod.io/new/#https://github.com/CobiontID/CobiontID.github.io/). A colab notebook with a more limited feature set and instructions is available [here](https://colab.research.google.com/github/CobiontID/CobiontID.github.io/blob/gh-pages/Readviz_demo.ipynb).

## Associated publications
*Phylogenomic analysis of Wolbachia genomes from the Darwin Tree of Life biodiversity genomics project* https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.3001972

*MarkerScan: Separation and assembly of cobionts sequenced alongside target species in biodiversity genomics projects* https://doi.org/10.12688/wellcomeopenres.20730.1
