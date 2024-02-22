# TransMuCoRes
This respository contains the source code and model checkpoints for the paper "Multilingual Coreference Resolution in Low-resource South Asian Languages" accepted at LREC-COLING 2024

## Dataset

TransMuCoRes dataset consists of translated dataset from OntoNotes and LitBank. We use the default train:dev:test splits of OntoNotes dataset whereas we had to split the LitBank dataset into train:dev:test.

Human annotated coreference resolution dataset in Hindi by Mujadia et al. (2016) was not in the CoNLL format. We converted the data to CoNLL format by automated scripts and few manual corrections. The resulting CoNLL formatted dataset was also splitted into train:dev:test splits.

CoNLL formatted files of the combined dataset is available [here](https://drive.google.com/file/d/1Jla-sg9sBoP58u6cC2BZ2HEme4AsQ1Ez/view?usp=sharing).

## Running Coreference Resolution 

### Installation
```pip install -r requirements.txt```

Multilingual coreference resolution model checkpoint is available [here](https://drive.google.com/file/d/19x6WY0fgf5E9phiaV6ORNxnhpg0GnY4w/view?usp=sharing). Place it inside the ```model``` folder.

### Inference

```python mcoref.py```

Modify the ```raw_sentences``` variable in ```mcoref.py``` to input any arbitary text to the coreference resolution model. Morever, the current code also supports pronomial resolution in Hindi sentences by resolving karak.

Takes 6 GB of GPU (if available) otherwise 6 GB on cpu.

## Citation

```
@misc{mishra2024multilingual,
      title={Multilingual Coreference Resolution in Low-resource South Asian Languages}, 
      author={Ritwik Mishra and Pooja Desur and Rajiv Ratn Shah and Ponnurangam Kumaraguru},
      year={2024},
      eprint={2402.13571},
      archivePrefix={arXiv},
      primaryClass={cs.CL}
}
```

If you use the multilingual coreference resolution model checkpoint from our work then consider citing the following as well:

```
@inproceedings{vladimir_dobrovolskii2021word,
  title={Word-Level Coreference Resolution},
  author={Dobrovolskii, Vladimir},
  booktitle={Proceedings of the 2021 Conference on Empirical Methods in Natural Language Processing},
  pages={7670--7675},
  year={2021}
}
```


If you use translated OntoNotes from our work then consider citing the following as well:

```
@article{weischedel2013ontonotes,
  title={Ontonotes release 5.0 ldc2013t19},
  author={Weischedel, Ralph and Palmer, Martha and Marcus, Mitchell and Hovy, Eduard and Pradhan, Sameer and Ramshaw, Lance and Xue, Nianwen and Taylor, Ann and Kaufman, Jeff and Franchini, Michelle and others},
  journal={Linguistic Data Consortium, Philadelphia, PA},
  volume={23},
  year={2013}
}
```

If you use translated LitBank from our work then consider citing the following as well:

```
@inproceedings{bamman2020annotated,
  title={An Annotated Dataset of Coreference in English Literature},
  author={Bamman, David and Lewke, Olivia and Mansoor, Anya},
  booktitle={Proceedings of the 12th Language Resources and Evaluation Conference},
  pages={44--54},
  year={2020}
}
```

If you use CoNLL formatted files of manually annotated dataset of Mujadia et al. (2016) from our work then consider citing the following as well:

```
@inproceedings{mujadia2016coreference,
  title={Coreference Annotation Scheme and Relation Types for Hindi},
  author={Mujadia, Vandan and Gupta, Palash and Sharma, Dipti Misra},
  booktitle={Proceedings of the Tenth International Conference on Language Resources and Evaluation (LREC'16)},
  pages={161--168},
  year={2016}
}
```