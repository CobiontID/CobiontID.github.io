---
title: An illustrated example
layout: page
toc: true
---


<style>
  #IDNAME {
  -moz-transform: scale(0.75, 0.75); 
  -webkit-transform: scale(0.75, 0.75); 
  -o-transform: scale(0.75, 0.75);
  -ms-transform: scale(0.75, 0.75);
  transform: scale(0.75, 0.75); 
  -moz-transform-origin: top left;
  -webkit-transform-origin: top left;
  -o-transform-origin: top left;
  -ms-transform-origin: top left;
  transform-origin: top left;
  display: block;
  vertical-align: bottom;
  padding: 0 !important;
  margin: 0 !important;
  }
</style>

# _Hylocomiadelphus triquetrus_ (big shaggy moss)

This example comes from the [From Specimens to Genomes](https://www.ebi.ac.uk/training/events/from-specimens-genomes/) course, and was chosen to illustrate that some samples can be tricky to unpick because they contain many different organisms. 

## Marker scan
HMM profiles of marker genes, such as rRNAs, which are well-sampled and conserved, are useful to get an overview of which species are present in a given sample. In this case, there is evidence of multiple bacteria, as indicated by the contigs containing bacterial SSUs reported in the table. The full table is available on the sample's [Tree of Life QC](https://tolqc.cog.sanger.ac.uk/darwin/non-vascular-plants/Hylocomiadelphus_triquetrus/) page (scroll down to the "SSU Marker species" section).

![image](https://user-images.githubusercontent.com/10507101/136378496-49eea402-3f95-427d-ac84-1ef33cc71ced.png)


## Composition analysis
### Scaffold tetranucleotide visualisation
The interactive plot below shows the canonical tetranucleotide counts for each scaffold reduced to two dimensions to allow visualisation.

<div>
<iframe
  src="https://cobiontid.github.io/examples/cbHylTriq8_scaffolds_multi_select.html"
  style="width:130%; height:650px;"  class="is-fullwidth"
  id="IDNAME">
</iframe>
</div>

As expected, this sample contains multiple clusters of contaminant scaffolds of microbial origin, in addition to the target genome (a non-vascular plant). Each scaffold is colour-coded by an additional sequence feature, to allow potential contamination to be spotted more easily. Contigs that are of interest can be selected with the lasso tool and downloaded.

#### Features (colours represent quantile bins)

| Label  | Feature | Notes |
| ------------- | ------------- | --- |
| "Hexamer"  | Estimated coding density | Expected to be higher in microbes than in animals, plants |
| "FastK" | Median number of times each large k-mer in the sequence occures across the whole assembly | Illustrates repetitiveness (for assembled sequences), k=60 in this example |
| "Unique_15mers" | Number of unique 15-mers per base pair | Captures sequence diversity |
| "Is_Connected" | Presence of at least one Hi-C connection to another scaffold | Absence of connections can highlight contaminants |
| "Connections_Base" | Number of Hi-C connections per base pair | |
| "Coverage" | Coverage estimates for hifiasm contigs | Not shown for scaffolds above |

### Read tetranucleotide visualisation

Because HiFi reads are both long and highly accurate, we can begin to assess incoming samples for contamination prior to assembly, and subsequently tie the results in with later steps. As with contigs and scaffolds, the tetranucleotides for each read can be reduced to 2D and annotated. Since a given read set typically contains millions of sequences, we implemented a variational autoencoder to project the data into two dimensions.

The plots below illustrate that the shaggy moss sample contains multiple groups of reads with high coding density and low coverage. Inspecting these clusters reveals that they contain bacterial sequences.

#### Reads labelled by estimated coding density
Purple: Low density. Yellow: High density. Note the high-density clusters on the right.

<img src="https://user-images.githubusercontent.com/10507101/135167436-cf040e7f-4645-418c-b193-37a3399ecf9d.png" width=500>

#### Reads labelled by median 60-mer count, approximating k-mer coverage
Purple: Low count. Yellow: High count. The target genome (moss), is present at fairly high coverage compared to the majority of the bacteria.

<img src="https://user-images.githubusercontent.com/10507101/135167487-f23c94e8-8909-4ccd-9261-6e5099ad26cb.png" width=500>

#### Reads labelled by marker scan pipeline results
Blue points represent reads flagged for removal. As we can see, the identified markers account for most, but not all of the groups of reads. As an additional step, we can therefore select sequences from the plot using an interactive widget, and query a database. Jump to [this page](reads.html) to explore an example of an insect read set in your browser.

<img src="https://user-images.githubusercontent.com/10507101/135230209-66049a04-f1b4-4e78-a600-bd4cf0e6bf6a.png" width=500>
