# CS 5640/6640 Final Project

**Project Name**: Extended Data Selection Using General-Purpose Transformer Models

**Authors**: Brandin Chase and Bryson Steck

## About

This notebook is our attempts to reimplement the FreeSel pipeline in use for numerical and natural language processing (NLP) data, using datasets with [motion caputre hand postures](https://archive.ics.uci.edu/dataset/405/motion+capture+hand+postures) and IMDB Comments respectively. 

## Running
This notebook was created and worked on in Google Colab.

To run the notebook, you can load it into Jupyter or Google Colab. Our code is not set up to take advantage of an NVIDIA GPU as we did not have the resources at this time. We have tested this notebook on the following:
- Google Colab (as of December 2024)
    - Python 3
    - CPU Compute Backend, 12GB RAM
        - You may run out of memory depending on your sample size, purchase a backend with more memory or run locally.
- Linux
    - Python 3.10 venv, 64GB RAM
        - Newer versions of Python **will not** work, you may need to download/install a second Python version.

## Experimentation

Unmodified, the notebook will set everything up and start experimenting with the parameters below. You can adjust them as you would like, given you have the time and resources. They are located in the second code cell.
```python
# The amount of samples to pull from the IMDB dataset.
# You may want to decrease this if running on Google Colab.
# Recommended values: 50-200
dataset_samples = 100

# The attention ratio.
# Recommended values: 0.1-0.9
tau = [0.2,0.4,0.6,0.8]

# The centroid number, used for clustering.
# We found modifying this value does not drastically change the FreeSel algorithm's effectiveness.
# Recommended values: [1, 3, 5, 7]
k = [3]

# The annotation budget size, controls the amount of "images" the FreeSel algorithm selects for the task model.
# Recommended values: 5%-50% of the dataset_samples variable
b = [dataset_samples * 0.10, dataset_samples * 0.30, dataset_samples * 0.50]
```

## Credits/References

- [Towards Free Data Selection with General-Purpose Models](https://proceedings.neurips.cc/paper_files/paper/2023/hash/047682108c3b053c61ad2da5a6057b4e-Abstract-Conference.html) (Reference Paper)
- [FreeSel GitHub Repository](https://github.com/yichen928/FreeSel/) (Original source code from the researchers in the above paper)
