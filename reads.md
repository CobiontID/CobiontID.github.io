---
title: Read visualisation
layout: page
show_sidebar: false
---

<style> #IDNAME { -moz-transform: scale(0.5, 0.5); -webkit-transform: scale(0.5, 0.5); -o-transform: scale(0.5, 0.5); -ms-transform: scale(0.5, 0.5); transform: scale(0.5, 0.5); -moz-transform-origin: top left; -webkit-transform-origin: top left; -o-transform-origin: top left; -ms-transform-origin: top left; transform-origin: top left; display: block; vertical-align: bottom; padding: 0 !important; margin: 0 !important; } </style>

## Using the interactive dashboard

There are two ways to exploring the data interactively. The first is the web app [here](https://huggingface.co/spaces/cc7740/read_VAE).

<iframe
	src="https://cc7740-read-vae.hf.space"
	frameborder="0"
	width="1450"
	height="750"
	id="IDNAME"
></iframe>

To experiment with loading your own data, you can also try the notebook version, which is more configurable but currently does not include the option to directly filter the data by taxonomic class.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/CobiontID/CobiontID.github.io/blob/main/Readviz_demo.ipynb)

The simplest way to run the notebook is to open it in Colab (you will not need to install anything on your local machine). Click on `Runtime -> Run all` at the top of the page. Continue with `Run anyway` if prompted that the notebook was not authored by Google. Then scroll down to interact with the plot.

### Filtering and querying data
For example, you may draw a rectangular selection and run blastn to find out what is in the cluster at the bottom with high coding density:

<img src="https://user-images.githubusercontent.com/10507101/214277601-9c4c1fd9-fd77-41fe-862d-932810451bfd.png" width=700>

You might also be interested in reads with k-mer coverage >= 1000. Notice the mitochondrion in the selection:

<img src="https://user-images.githubusercontent.com/10507101/214279741-e667a16c-62df-42b2-b3b1-25a24818e93c.png" width=700>

There is also some low-coverage bacterial contamination hiding in the plot. Try setting the range to 0-15 and changing the background colour to make the points easier to see (the webapp version also supports reversing the colour map):

<img src="https://user-images.githubusercontent.com/10507101/214903678-d281d170-a272-45b8-b051-14f2dfd8947b.png" width=700>

## Cross-referencing other sources of information
The section below the dashboard shows how read visualisation can be combined with existing labels for more efficient data exploration. The example below shows the reads flagged as trypanosome by marker scan in red. Reads that map to the mitochondrial assembly are shown in gold. All other (unlabelled) points in blue. Notice that the main "trypanosome" cluster corresponds to the coding dense cluster mentioned above.

<img src="https://user-images.githubusercontent.com/10507101/216154074-154908f0-3542-49e9-bf0e-39c7f7718705.png" width=700>

## Using your own data
To explore your own data with the notebook, you can upload your own files and adjust the configuration. More details are provided in the notebook. However, since fasta files can be very large, it will probably be more convenient to download the notebook and run it locally with Jupyter (it will also work in Virtual Studio Code).



