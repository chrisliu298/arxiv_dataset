# ArXiv Dataset

This repo contains a part of the dataset from [arxiv_archive](https://github.com/staeiou/arxiv_archive). Specifically, it contains papers under aritficial intelligence (AI), machine learning (LG), computation and language (CL), and computer vision and pattern recognition (CV) categories. 

I use the titles and abstract of these papers to fine-tune my GPT-2 model.

## Usage

The script reads the `.tsv` file, adds special symbols to separate the titile and the abstract, and writes a text file for each category and an extra file of shuffled instances. It splits all examples into training, validation, and test sets.

```shell
python preprocess_arxiv.py
```

## Dataset

|                   Category                   |   Count    | Percentage (%) | BPE Token Count |
| :------------------------------------------: | :--------: | :------------: | :-------------: |
|         Artificial Intelligence (AI)         |   21889    |     18.00      |    4,791,146    |
|            Machine Learning (LG)             |   47025    |     38.67      |   11,078,662    |
|        Computation and Language (CL)         |   17008    |     13.99      |    3,549,625    |
| Computer Vision and Pattern Recognition (CV) |   35694    |     29.35      |    8,687,225    |
|                  **Total**                   | **121616** |    **100**     | **28,106,658**  |

|   Splits   |   Count    | Percentage (%) | BPE Token Count |
| :--------: | :--------: | :------------: | :-------------: |
|   Train    |   109616   |     90.13      |   25,201,566    |
| Validation |    6000    |      4.93      |    1,435,898    |
|    Test    |    6000    |      4.93      |    1,469,196    |
| **Total**  | **121616** |    **100**     | **28,106,660*** |

**Note:** The two extra tokens here are the `\n`'s at the bottom of the file.

## Reference

```
R. Stuart Geiger (2020). "ArXiV Archive: A Tidy and Complete Archive of Metadata for Papers on arxiv.org." Zenodo. http://doi.org/10.5281/zenodo.1463242
```

