## Positional Embeddings and Zero-shot Learning using BERT for Molecular-Property Prediction

This is a Pytorch code and proposed datasets of our paper. The code has been tested on PyTorch 2.2.   
To install the dependencies, please run:
```bash
pip install -r requirements.txt
```

### Pre-Training

#### Model Configuration

|Model|Hidden-Size|num_hidden_layers|num_attention_heads|hidden_act|max_sequence_length|vocab_size|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|BERT-base|768|12|12|GELU|512|592|

#### Model Size

|PEs|# of Params|
|:---:|:---:|
|Absolute|85,054,464|
|Relative_Key|85,840,128|
|Relative_Key_Query|85,840,128|
|Sinusoidal|85,054,464|

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
