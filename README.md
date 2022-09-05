# Extended Essay-BR

This repository is an extended version of the Essay-BR corpus detailed [here](https://sol.sbc.org.br/index.php/dsw/article/view/17414).
It contains essays written by high school Brazilian students. 
These essays were graded by humans professionals following the criteria of the ENEM exam.

## Reference

```
@article{marinho-et-al-22,
  author = {Jeziel Marinho and Rafael Anchiêta and Raimundo Moura},
  title = {Essay-BR: a Brazilian Corpus to Automatic Essay Scoring Task},
  journal = {Journal of Information and Data Management},
  year = {2022},
  volume = {13}
  number = {1},
  pages = {65--76},
  publisher = {Sociedade Brasileira de Computação},
  doi = {10.5753/jidm.2022.2340},
  url = {https://sol.sbc.org.br/journals/index.php/jidm/article/view/2340}
}
```

## Requirements

- Python (version 3.6 or later)
- `pip install -r requirements.txt`

## Usage
To read the corpus, follow these steps:

````python
>>> from build_dataset import Corpus

>>> c = Corpus()

>>> train, valid, test = c.read_splits()

>>> train.head()
>>> 
>>>      prompt                                        title      ...   c5  score
>>> 0      86                                    Bem está mental  ...  160   680
>>> 1      86  A questão das redes sociais na saúde mental da...  ...  160   880
>>> 2      47          Democratização do ensino remoto no Brasil  ...  160   800
>>> 3      89  ZZZ (POR FAVOR, IGNOREM O TAMANHO, PRECISO DA ...  ...  200   880
>>> 4      40                   Um samba enredo que está por vir  ...  200   840

>>> valid.head()
>>> 
>>>      prompt                                        title   ...   c5  score
>>> 0     128  O papel do meio ambiente na riqueza de um país  ...   80    440
>>> 1      93                                             NaN  ...  120    640
>>> 2      92                      Não ao preconceito amarelo  ...  160    840
>>> 3      71                  Suicidío, problema ou solução?  ...   80    440
>>> 4      66                                             NaN  ...   80    440

>>> test.head()
>>> 
>>>      prompt                    title      ...   c5  score
>>> 0      58      O planeta precisa de você  ...   40    440
>>> 1      50           Belicismo científico  ...  120    760
>>> 2      82                            NaN  ...  160    720
>>> 3      58     Consumismo e Meio Ambiente  ...   40    440
>>> 4      95  Debate sobre o marco temporal  ...  160    720
