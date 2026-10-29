# KE-GCN: Knowledge-Enhanced Graph Convolutional Network for Multimodal Aspect-Based Sentiment Analysis

This is a official implementation of **KE-GCN**, a knowledge-enhanced graph convolutional network for multimodal aspect-based sentiment analysis (MABSA).


## Research overview

MABSA predicts sentiment toward a specific aspect in a post by using both the post text and its associated image. The KE-GCN has three major components:

- **Knowledge-Enhanced Textual Sentiment Module:** uses syntactic structure with affective and commonsense knowledge.
- **Knowledge-Enhanced Visual Sentiment Module:** uses text-guided visual representations and graph reasoning.
- **Text–Visual Alignment Module:** encodes the tweet and an image caption to provide global cross-modal context.

The paper evaluates the approach on the Twitter-2015 and Twitter-2017 benchmark datasets.

## Repository contents

| File | Purpose |
|---|---|
| `ke-gcn-training.ipynb` | Model definition, training, and evaluation notebook supplied for the project. |
| `ke-gcn-graph-preprocessing.ipynb` | Graph and feature preprocessing notebook. |
| `ke-gcn-conceptnet-cache.ipynb` | ConceptNet cache preparation notebook. |
| `ke-gcn-senticnet-coverage.ipynb` | SenticNet coverage analysis notebook. |
| `requirements.txt` | Core Python dependencies referenced by the notebooks. |
| `CITATION.cff` | Citation metadata for the associated paper. |


## Datasets and external resources

The paper identifies the Twitter-2015 and Twitter-2017 MABSA datasets and points to the following source:

- [TwitterDataMABSA dataset repository](https://github.com/CopotronicRifat/TwitterDataMABSA)
- [ConceptNet](https://github.com/commonsense/conceptnet5/wiki)
- [SenticNet](https://sentic.net/)



## Environment setup

Use Python with a compatible PyTorch installation. For GPU use, install the PyTorch build appropriate for your CUDA environment from the [official PyTorch installation selector](https://pytorch.org/get-started/locally/) before installing the remaining packages.

```bash
pip install -r requirements.txt
```



