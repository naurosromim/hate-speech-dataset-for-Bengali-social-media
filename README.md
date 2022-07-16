# BD-SHS: A Benchmark Dataset for Learning to Detect Online Bangla Hate Speech in Different Social Contexts

For more detail, you can check [our paper.](http://www.lrec-conf.org/proceedings/lrec2022/pdf/2022.lrec-1.552.pdf)

## Abstract

Social media platforms and online streaming services have spawned a new breed of Hate Speech (HS). Due to the massive amount of user-generated content on these sites, modern machine learning techniques are found to be feasible and cost-effective to tackle this problem. However, linguistically diverse datasets covering different social contexts in which offensive language is typically used are required to train generalizable models. In this paper, we identify the shortcomings of existing Bangla HS datasets and introduce a large manually labeled dataset BD-SHS that includes HS in different social contexts. The labeling criteria were prepared following a hierarchical annotation process, which is the first of its kind in Bangla HS to the best of our knowledge. The dataset includes more than 50,200 offensive comments crawled from online social networking sites and is at least 60% larger than any existing Bangla HS datasets. We present the benchmark result of our dataset by training different NLP models resulting in the best one achieving an F1-score of 91.0%. In our experiments, we found that a word embedding trained exclusively using 1.47 million comments from social media and streaming sites consistently resulted in better modeling of HS detection in comparison to other pre-trained embeddings.

## Dataset details

You can find the dataset [here.](https://www.kaggle.com/datasets/naurosromim/bdshs)

**abbreviations used:**

`HS` => `hate speech`

`NH` => `not hate speech`

`ind` => `Individual`

| Task  | Task description    | # labels | Labels                                            | Nature of classification |
| ----- | ------------------- | -------- | ------------------------------------------------- | ------------------------ |
| TaskA | HS detection        | 02       | `HS`, `NH`                                        | Binary (HS or NH)        |
| TaskB | HS target detection | 04       | `ind`, `male`, `female`, `group`                  | Multilabel               |
| TaskC | HS type detection   | 04       | `slander`, `religion`, `gender`, `callToViolence` | Multilabel               |

## Usage

- Download data from [here](https://www.kaggle.com/datasets/naurosromim/bdshs). Create a folder named `dataset`  and place `train.csv`, `val.csv` and `test.csv` files there.

- `jupyter notebooks` folder contains `taskA-SVM`, `taskA-BiLSTM`, `taskB-SVM`, `taskB-BiLSTM`, `taskC-SVM`, `taskC-BiLSTM`.

- `embedding` folder contains pretrained word embeddings **Informal FastText (IFT)**. Other embeddings have to be downloaded from given sources.
  
  - `MFT`: Download from [here](https://dl.fbaipublicfiles.com/fasttext/vectors-crawl/cc.bn.300.bin.gz). Or, you can learn more about it's documentation from [https://fasttext.cc/](https://fasttext.cc/)
  
  - `BFT`: Download from [here](https://github.com/rezacsedu/Classification_Benchmarks_Benglai_NLP#pre-trained-bengfasttext-model). 

## Requirements

- python 3.8 or higher

- pandas 1.3.5

- numpy 1.21.5

- nltk 3.2.5

- scikit learn 1.0.2

- keras 2.8

- gensim 3.6

## Authors

* Syed Nauros Hossain Romim <sup>1</sup>

* Mosahed Ahmed <sup>1</sup>

* Md Saiful Islam <sup>1, 2</sup>

* Arnab Sen Sharma<sup>1</sup>

* Hriteshwar Talukdar <sup>1,3</sup>

* Mohammad Ruhul Amin <sup>4</sup>
  
  <sup>1</sup> Shahjalal University of Science and Technology, Bangladesh

  <br>
  <sup>2</sup> University of Alberta, Canada
  <br>
  <sup>3</sup> University of Boston, USA
  <br>
  <sup>4</sup> Fordham University, USA

## Bibtex

```
@InProceedings{romim-EtAl:2022:LREC,
  author    = {Romim, Nauros  and  Ahmed, Mosahed  and  Islam, Md Saiful  and  Sen Sharma, Arnab  and  Talukder, Hriteshwar  and  Amin, Mohammad Ruhul},
  title     = {BD-SHS: A Benchmark Dataset for Learning to Detect Online Bangla Hate Speech in Different Social Contexts},
  booktitle      = {Proceedings of the Language Resources and Evaluation Conference},
  month          = {June},
  year           = {2022},
  address        = {Marseille, France},
  publisher      = {European Language Resources Association},
  pages     = {5153--5162},
  abstract  = {Social media platforms and online streaming services have spawned a new breed of Hate Speech (HS). Due to the massive amount of user-generated content on these sites, modern machine learning techniques are found to be feasible and cost-effective to tackle this problem. However, linguistically diverse datasets covering different social contexts in which offensive language is typically used are required to train generalizable models. In this paper, we identify the shortcomings of existing Bangla HS datasets and introduce a large manually labeled dataset BD-SHS that includes HS in different social contexts. The labeling criteria were prepared following a hierarchical annotation process, which is the first of its kind in Bangla HS to the best of our knowledge. The dataset includes more than 50,200 offensive comments crawled from online social networking sites and is at least 60\% larger than any existing Bangla HS datasets. We present the benchmark result of our dataset by training different NLP models resulting in the best one achieving an F1-score of 91.0\%. In our experiments, we found that a word embedding trained exclusively using 1.47 million comments from social media and streaming sites consistently resulted in better modeling of HS detection in comparison to other pre-trained embeddings. Our dataset and all accompanying codes is publicly available at github.com/naurosromim/hate-speech-dataset-for-Bengali-social-media},
  url       = {https://aclanthology.org/2022.lrec-1.552}
}

```
