---
title: CobiontID overview
layout: page
show_sidebar: false
menubar: docs_menu

---
# Identifying cobionts and contaminants

Disentangling sequences from different sources can be both interesting and challenging. It can reveal interactions between organisms and their genomes through time (considering extant associations and molecular fossils). In some cases, the aim may simply be to remove contamination that has found its way into a sample. However, determining where a sequence came from is not always straightforward - especially when exploring less well sampled parts of the tree of life, where few close relatives have been sequenced.

On these pages, you will find some examples showing how we are tackling this issue in the <a href="https://www.sanger.ac.uk/programme/tree-of-life/">Tree of Life</a> programme. Our approach, which is tailored for HiFi data, combines grouping sequences from the same source with finding reliable taxonomic hints. This allows us to reduce reliance on databases, which can be incomplete and contain mislabelled sequences.

<img src="https://user-images.githubusercontent.com/10507101/135228070-aca877cf-d210-4e65-8805-a679158b68e2.png" width=300>

## The CobiontID approach

The **CobiontID** process has two parts: First, **Marker scan** provides taxonomic information. HMM profiles of marker genes, such as rRNAs, which are well-sampled and conserved, are useful to classify sequences from genomes that are otherwise too diverged from their closest sequenced relative. We can therefore gauge which species are present in a given sample, and construct streamlined databases for read classification. Second, a combination of assembly, read mapping and **compositional clustering** allows the sequences to be assigned to groups that can be tagged with this taxonomic information.

See [here] for an illustration of how these tools can be used.

[here]: examples.html

## Additional information
- ![image](https://user-images.githubusercontent.com/10507101/214304451-5c5f4a0f-b0f1-485e-afe8-0eea4b592475.png) [GitHub](https://github.com/CobiontID/)
- [Slides](https://drive.google.com/file/d/1ghtPRkdNZRLfDH-pTluUJ2Xq1IpKRaht/view) from talk on CobiontID at PopGroup55 (2022)
- [Flash presentation](https://twitter.com/cc7740/status/1479071728697548807) accompanying PopGroup talk
