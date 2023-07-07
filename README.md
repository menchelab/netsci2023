# netsci2023


# VR Material - Overview

This repository contains a collection of notebooks for generating VR content using the Barabasi-Albert network and expression profiles data. Each notebook focuses on different aspects of the VR visualization process.

## Basic Barabasi-Albert Network

[Google colab notebook](https://drive.google.com/file/d/1D0ZJWeCBZnKMDbemrFh4j1_xMa0vzjxf/view?usp=sharing)

The `basic_barabasi_albert.ipynb` notebook demonstrates the basic upload functionalities. It generates a random BA Graph using the `networkx` module and converts the node and edge structure into a JSON file required for the VR platform. The notebook introduces two core functions, `make_json()` and `plotly_preview()`, which will be used in other notebooks as well. It showcases the minimal usage of `make_json()` to quickly generate the first VR content.

## Celltype Network

[Google colab notebook](https://drive.google.com/file/d/16ZEDlMoRDkPgqdZ8syhb05wAk8XwKgRI/view?usp=sharing)

The `celltype_network.ipynb` notebook constructs a network based on expression profiles from The Human Protein Atlas. In this network, cell types are represented as nodes, and links are shared genes between cell types. Edge weights are calculated using the Jaccard similarity score, measuring the number of shared genes.

This notebook showcases three main steps:

1. **Edge Filtering**: Edges are ranked and filtered based on edge-betweenness-centrality, with a chosen cutoff criterion. The aim is to retain the minimal set of edges before the network breaks down.

2. **Layouts**: Different layouts are introduced for network visualization. Initially, random and spring layouts provide basic placement of the nodes. More advanced layouts such as 'global' and 'importance' from Cartographs can be employed. Additionally, the concept of utilizing the z-axis is introduced to display an external attribute, where the number of different tissues a cell type can be found in is used as the value for the z-axis.

3. **Coloring and Annotations**: This section demonstrates coloring nodes and edges and transferring node annotations into the JSON format. This allows the annotations to be visible and accessible within the VR environment.

## Edge Filtering

[Google colab notebook](https://drive.google.com/file/d/1VJ-ikQcHgxb0b0RAj46BbDUIuirHZ6-v/view?usp=sharing)


The `edge_filtering.ipynb` notebook demonstrates three different edge filtering methods for the expression profiles dataset:

1. **Cutoff by Edge Weights Directly**
2. **Edge Betweenness Centrality**
3. **Disparity Filter (Backbone)**

Each method is explored in detail within the notebook.

Feel free to explore the notebooks and use them to generate VR content for your projects!



## Further links

[The VR backend github repository](https://github.com/menchelab/DataDiVR_WebApp)


[A handbook that covers the main features of the interactive panels in VR](https://docs.google.com/document/d/1L_ag88HSlDYvVnmJYiouArNd49CO7_sSKbpwvjgwquo/edit?usp=sharing)