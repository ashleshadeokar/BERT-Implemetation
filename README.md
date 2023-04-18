# BERT-Implemetation

# Implement BERT 
 developing a minimalist version of BERT.

Perform sentence classification on two datasets: the ``sst`` dataset and the ``cfimdb`` dataset with your BERT model.


### Important Notes
* Follow `setup.sh` to properly setup the environment and install dependencies. Make sure to do the rest of your work on the appropriate environment.
* There is a detailed description of the code structure in [structure.md](./structure.md), including a description of which parts you will need to implement.

```
mkdir -p 
python3 classifier.py --option [pretrain/finetune] --epochs NUM_EPOCHS --lr LR --train data/sst-train.txt --dev data/sst-dev.txt --test data/sst-test.txt
```

## Reference accuracies: 
Mean reference accuracies over 10 random seeds with their standard deviation shown in brackets.
Pretraining for SST:
Dev Accuracy: 0.313
Test Accuracy: 0.303

Finetuning for SST:
Dev Accuracy: 0.515 (0.004)
Test Accuracy: 0.526 (0.008)

Finetuning for CFIMDB:
Dev Accuracy: 0.588
Test Accuracy: 0.713


`prepare_submit.py` can help to create(1) or check(2) the to-be-submitted zip file. It will throw assertion errors if the format is not expected, and we will *not accept submissions that fail this check*. Usage: (1) To create and check a zip file with your outputs, run `python3 prepare_submit.py path/to/your/output/dir `, (2) To check your zip file, run `python3 prepare_submit.py path/to/your/submit/zip/file.zip `


### Acknowledgements

_This assignment is adapted from the Carnegie Mellon University's CS11-711 course and the minBERT assignment created by Shuyan Zhou, Zhengbao Jiang, Ritam Dutt and Brendon Boldt._

Parts of the code are from the [`transformers`](https://github.com/huggingface/transformers) library ([Apache License 2.0](./LICENSE)).
