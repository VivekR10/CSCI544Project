# CSCI544Project
## Densely Interactive Inference Network (DIIN)
This is the code to reproduce the model in [Natural Language Inference over Interaction Space](https://arxiv.org/abs/1709.04348) and contains code for proposed improvements on the current baseline model. 
### Environment
The environment setup needs to have at least 30GB RAM and 16 GB GPU memory for the code to run. We use a GCP instance with Tesla P100 GPU and intalled c2-deeplearning-pytorch-1-2-cu100-20191005 image.
### Setup
- $ git clone https://github.com/VivekR10/CSCI544Project.git
- $ cd DIIN/DIIN_PyTorch
- $ python download.py
- BERT embedding can be downloaded either by running BERT.ipynb notebook that we have provided or from https://drive.google.com/drive/folders/1zBjsZzBHf7KGfMr0dWIu8wJv1cPlKWRA?usp=sharing
In this Logs folder, go to logs_bert for embeddings of BERT 768 model and logs_bert2 for embeddings of BERT 1024 model.

### Execution
- $ cd pytorch
- For the baseline model, run $ python train_snli_pytorch.py DIIN demo_testing_SNLI --training_completely_on_snli --cuda --use_dense_net
- For the BERT 768 model + DenseNet use the respective embeddings file provided in drive link above and run                                $ python train_snli_pytorch.py DIIN demo_testing_SNLI --training_completely_on_snli --cuda --bert --use_dense_net
- For the BERT 1024 model + DenseNet use the respective embeddings file provided in drive link above and run                               $ python train_snli_pytorch.py DIIN demo_testing_SNLI --training_completely_on_snli --cuda --bert --use_dense_net
- For Glove + RESNET model, run $ python train_snli_pytorch.py DIIN demo_testing_SNLI --training_completely_on_snli --cuda
- For the BERT 768 model + RESNET use the respective embeddings file provided in drive link above and run $ python train_snli_pytorch.py DIIN demo_testing_SNLI --training_completely_on_snli --cuda --bert
- For the BERT 1024 model + RESNET use the respective embeddings file provided in drive link above and run $ python train_snli_pytorch.py DIIN demo_testing_SNLI --training_completely_on_snli --cuda --bert
