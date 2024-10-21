### ArtExp

In this folder, we provide a Jupyter Notebook to perform the training of the art experts and the export of the features used by the main repo. As mentioned in the paper, the implementation details are slightly different, as we used torchvision 0.16.2 and pytorch 2.1.2. The two files ```my_genre_style_{train,val}.csv``` contain the train/val split we used to perform multitask classification, starting from the original annotations found in ```wikiart_csv```. These, along the folder ```wikiart``` (not attached to this repo), are obtained from https://github.com/cs-chan/ArtGAN/tree/master/WikiArt%20Dataset. We thank the authors for releasing the data.

### Citations

If you found anything useful from this folder, as well as from the main repo, please consider citing our paper.

CITATION SOON