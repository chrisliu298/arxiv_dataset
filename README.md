# ArXiv Dataset

This repo contains a part of the dataset from [arxiv_archive](https://github.com/staeiou/arxiv_archive). Specifically, it contains papers under aritficial intelligence (AI), machine learning (LG), computation and language (CL), and computer vision and pattern recognition (CV) categories. 

I use the titles and abstract of these papers to fine-tune my GPT-2 model.

## Usage

The script reads the `.tsv` file, adds special symbols to separate the titile and the abstract, and writes a text file for each category and an extra file of shuffled instances. It splits all examples into training, validation, and test sets.

```shell
python preprocess_arxiv.py
```

## Dataset

|   Splits   |   Count    | Percentage (%) | BPE Token Count |
| :--------: | :--------: | :------------: | :-------------: |
|   Train    |   90,000   |     90.11      |   20,834,012    |
| Validation |    4,940   |      4.95      |    1,195,056    |
|    Test    |    4,940   |      4.95      |    1,218,754    |
| **Total**  | **99880**  |    **100**     | **23,247,822**  |

**Note:** The two extra tokens here are the `\n`'s at the bottom of the file.

## Reference

```
R. Stuart Geiger (2020). "ArXiV Archive: A Tidy and Complete Archive of Metadata for Papers on arxiv.org." Zenodo. http://doi.org/10.5281/zenodo.1463242
```

