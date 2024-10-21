# HierArtEx: Hierarchical Representations and Art Experts Supporting the Retrieval of Museums in the Metaverse

This code accompanies the paper "HierArtEx: Hierarchical Representations and Art Experts Supporting the Retrieval of Museums in the Metaverse" accepted for presentation at [MMM 2025](https://mmm2025.net/). [DOI]() [preprint]()

![Overview of HierArtEx](assets/architecture.png?raw=true)

Abstract:
```The improvements in Virtual Reality technologies are bringing more attention to the Metaverse and the nearly unlimited experiences available there. Among these, digital museums have seen an increase in the number of yearly visitors, especially after the COVID-19 pandemics. However, no tools are available to support the user in the searching process. To this end, we start investigating the Text-to-Museum retrieval task, involving museums composed of many rooms enriched by multimedia elements affecting their relevance to the user query. To model this complex type of data, we design HierArtEx, which leverages hierarchical representations to model the whole museum, while combining generic and art-specific knowledge for capturing the visual contents of each single room. We validate its effectiveness on Museums3k, a large dataset that we collect, containing 3000 realistic museums each annotated by a description of its contents. Moreover, qualitative analyses confirm favorable results and their alignment with real user queries, while also highlighting the shortcomings of standard evaluation protocols in retrieval, as they fail to capture all relevant museums.```

### General info on the structure

The repository contains three Jupyter Notebooks for the HierArtEx method (Complex3DScenesRetrieval_HierArtEx_CameraReady.ipynb), the method without the art experts (Complex3DScenesRetrieval_HierArtEx_wo_ArtExp_CameraReady.ipynb), and the baseline (Complex3DScenesRetrieval_Baseline_CameraReady.ipynb). It further includes a Jupyter Notebook for the qualitative analysis reported in the paper (QualitativeAnalysis_CameraReady.ipynb), and a folder containing the details on how we trained the art experts. The train/val/test split is available in ```indices_museum_dataset.pkl```.

### Data

![Example from the dataset](assets/dataset_example.png?raw=true)

In this work, we relied on pre-extracted features from the Museums3k dataset (available [here](https://github.com/aliabdari/Museums3k)). In each museum, twelve screenshots are taken by rotating a camera within each room. The features are extracted using a pretrained CLIP, and are found in the path ```notebook/tmp_museums/open_clip_features_museums3k/images```. Additionally, a paragraph is created for each museum depicting its contents. The features for these are found in the path ```notebook/tmp_museums/open_clip_features_museums3k/descriptions/tokens_strings```. Raw descriptions are also found in the folder ```sentences``` (used for analysis and visualization purposes). The features extracted from the art experts are found in the folders starting with ```preextracted_vectors_wikiart```. They were extracted using the art experts we pretrained on WikiArt.

### Citation

SOON

### Acknowledgements

This work was supported by MUR PRIN (Progetti di Ricerca di Rilevante Interesse Nazionale, Project code 2022YTE579_001 - CUP G53D23002930006) and by the EU (NextGenerationEU - PNRR M4.C2.1.1), and by the Department Strategic Plan (PSD) of the University of Udine - Interdepartmental Project on Artificial Intelligence (2020-25).
