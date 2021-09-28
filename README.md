# CobiontID

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

Disentangling sequences from different sources can be both interesting and challenging. It can reveal interactions between organisms and their genomes through time (considering extant associations and molecular fossils), but determining where a sequence came from is not always straightforward - especially when exploring less well sampled parts of the tree of life, where few close relatives have been sequenced.

Below, you will find some examples illustrating how we are tackling this issue in the <a href="https://www.sanger.ac.uk/programme/tree-of-life/">Tree of Life</a> programme. Our approach, which is tailored for HiFi data, combines grouping sequences from the same source with finding reliable taxonomic hints.

## Example: _Hylocomiadelphus triquetrus_ (big shaggy moss)
### Composition analysis
#### Scaffold tetranucleotide visualisation for _Hylocomiadelphus triquetrus_
The interactive plot below shows the canonical tetranucleotide counts for each scaffold reduced to two dimensions to allow visualisation.

<div>
<iframe
  src="./examples/cbHylTriq8_scaffolds_multi_select.html"
  style="width:130%; height:650px;"  class="is-fullwidth"
  id="IDNAME">
</iframe>
</div>

This sample contains multiple clusters of contaminant scaffolds of microbial origin, in addition to the target genome (a non-vascular plant). Each scaffold is colour-coded by an additional sequence feature, to allow potential contamination to be spotted more easily. Contigs that are of interest can be selected with the lasso tool and downloaded.

##### Features (colours represent quantile bins)
- "Hexamer": Estimated coding density
- "FastK": The median number of times each 60-mer in the sequence occures across the whole assembly (illustrates repetitiveness)
- "Unique_15mers": Number of unique 15-mers per base pair (illustrates sequence diversity)
- "Is_Connected": Presence of at least one Hi-C connection to another scaffold (absence of connections can indicate contamination)
- "Connections_Base": Number of Hi-C connections per base pair

#### Read tetranucleotide visualisation for _Hylocomiadelphus triquetrus_

<img src="https://user-images.githubusercontent.com/10507101/135167436-cf040e7f-4645-418c-b193-37a3399ecf9d.png" width=500>
<img src="https://user-images.githubusercontent.com/10507101/135167487-f23c94e8-8909-4ccd-9261-6e5099ad26cb.png" width=500>
