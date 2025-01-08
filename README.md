## Positional Embeddings and Zero-shot Learning using BERT for Molecular-Property Prediction

<img src="https://github.com/user-attachments/assets/b6dc1a35-736e-46a6-b7cd-68a860526a74" width="80%"></img>


This is a Pytorch code and proposed datasets of our paper. The code has been tested on PyTorch 2.2.   
To install the dependencies, please run:
```bash
pip install -r requirements.txt
```

### Datasets
The dataset was sourced from publicly available databases and previous studies except for newly proposed datasets(Antimalarial, Cocrystals, COVID, COVID-19)

|Usage|Data|Task type|# Compounds|
|:---:|:---:|:---:|:---:|
|Pre-Training|ZINC, PubChem, <br> ChEMBL, Research studies| - | 7,949,003|
|Fine-Tuning|  ESOL |Regression| 1,128|
|Fine-Tuning|  FreeSolv |Regression| 642|
|Fine-Tuning|  Lipophilicity |Regression| 4,200|
|Fine-Tuning|  BBBP |Classification| 2,039|
|Fine-Tuning|  Tox21 |Classification| 7,831|
|Fine-Tuning|  ClinTox |Classification| 1,478|
|Fine-Tuning|  SIDER |Classification| 1,427|
|Fine-Tuning|  Antimalarial |Classification| 4,794|
|Fine-Tuning|  Cocrystals |Classification| 3,282|
|Fine-Tuning|  COVID |Classification| 740|
|Fine-Tuning|  COVID-19 |Classification| 2,601|



### Pre-Training

#### Model Configuration

|Model|Hidden-Size|# of hidden_layers|# of attention_heads|hidden_act|max_sequence_length|vocab_size|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|BERT-base|768|12|12|GELU|512|592|

#### Model Training

We pre-train the model with 2 or 4 NVIDIA GeForce RTX 3090 GPUs.

|PEs|# of Params|Training Time (h)|Training Accuracy|
|:---:|:---:|:---:|:---:|
|Absolute|85,054,464|167 | 0.9568|
|Relative_Key|85,840,128|180| 0.9746|
|Relative_Key_Query|85,840,128|120| 0.9763|
|Sinusoidal|85,054,464|105 |0.9755|

### Fine-Tuning

### Citation

If you find this code or dataset useful for your research or applications, please consider citing it using the following BibTeX:

```
To be added
```

### Acknowledgement

Our implementation is built upon resources from [Huggingface Transformers](https://github.com/huggingface/transformers).
We also borrow the fine-tuning datasets from [MoleculeNet](https://moleculenet.org/).   
We extend our gratitude to the original authors for open-sourcing their work.
