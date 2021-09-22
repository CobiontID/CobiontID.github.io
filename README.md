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
  }
</style>
## Example: _Hylocomiadelphus triquetrus_ (big shaggy moss)
### Composition analysis
#### Scaffold tetranucleotide visualisation for _Hylocomiadelphus triquetrus_
The frame below displays the canonical tetranucleotide counts for each scaffold reduced to two dimensions to allow visualisation. Each scaffold is colour-coded by an additional feature (binned into quantiles), to allow potential contamination to be spotted more easily. Contigs that are of interest can be selected with the lasso tool and downloaded.

<iframe
  src="./examples/cbHylTriq8_scaffolds_multi_select.html"
  style="width:130%; height:800px;"  class="is-fullwidth"
  id="IDNAME"
></iframe>

##### Features
- "Hexamer": Estimated coding density
- "FastK": The median number of times each 60-mer in the sequence occures across the whole assembly (illustrates repetitiveness)
- "Unique_15mers": Number of unique 15-mers per base pair (illustrates sequence diversity)
- "Is_Connected": Presence of at least one Hi-C connection to another scaffold (absence of connections can indicate contamination)
- "Connections_Base": Number of Hi-C connections per base pair
