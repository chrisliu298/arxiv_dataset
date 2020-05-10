# ArXiv Dataset

This repo contains a part of the dataset from [arxiv_archive](https://github.com/staeiou/arxiv_archive). Specifically, it contains papers under aritficial intelligence (AI), machine learning (LG), computation and language (CL), and computer vision and pattern recognition (CV) categories. 

I use the titles and abstract of these papers to fine-tune my GPT-2 model.

## Usage

The script reads the `.tsv` file, adds special symbols to separate the titile and the abstract, and writes a text file for each category and an extra file of shuffled instances. Then it splits the training and evaluation data at the ratio 9:1.

```shell
python make_arxiv_data.py
```

## Dataset

|                   Category                   |   Count    |
| :------------------------------------------: | :--------: |
|         Artificial Intelligence (AI)         |   21889    |
|            Machine Learning (LG)             |   47025    |
|        Computation and Language (CL)         |   17008    |
| Computer Vision and Pattern Recognition (CV) |   35694    |
|                  **Total**                   | **121616** |

## Reference

```
R. Stuart Geiger (2020). "ArXiV Archive: A Tidy and Complete Archive of Metadata for Papers on arxiv.org." Zenodo. http://doi.org/10.5281/zenodo.1463242
```

