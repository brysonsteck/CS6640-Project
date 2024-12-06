# CS 5640/6640 Final Project

**Project Name**: Extended Data Selection Using General-Purpose Transformer Models

**Authors**: Brandin Chase and Bryson Steck

## About

This notebook is our attempts to reimplement the FreeSel pipeline in use for numerical and natural language processing (NLP) data, using datasets with [motion caputre hand postures](https://archive.ics.uci.edu/dataset/405/motion+capture+hand+postures) and IMDB Comments respectively. 

## Running
This notebook was created and worked on in Google Colab.

To run the notebook, you can load it into Jupyter or Google Colab. Running on a local machine is preferred as, depending on your sample sizes, you may run out of memory. 

## Experimentation

Unmodified, the notebook will set everything up and start experimenting with the following parameters:
```python
# The amount of samples to pull from the IMDB dataset.
# Found in code cell 2.
dataset_samples = 100

# The attention ratio
# Found in the last code cell.
tau = [0.2,0.4,0.6,0.8]

k = [3]
b = [dataset_samples * 0.10, dataset_samples * 0.30, dataset_samples * 0.50]:
```

## Credits/References

- [Towards Free Data Selection with General-Purpose Models](https://proceedings.neurips.cc/paper_files/paper/2023/hash/047682108c3b053c61ad2da5a6057b4e-Abstract-Conference.html) (Reference Paper)
- [FreeSel GitHub Repository](https://github.com/yichen928/FreeSel/) (Source Code of the above paper's researchers )
