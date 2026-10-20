# KE-GCN: Knowledge-Enhanced Graph Convolutional Network for Multimodal Aspect-Based Sentiment Analysis

This repository organizes the supplied research notebooks associated with **KE-GCN**, a knowledge-enhanced graph convolutional network for multimodal aspect-based sentiment analysis (MABSA).

The notebooks have been renamed and project identifiers have been rebranded to KE-GCN. The underlying experimental approach and saved notebook outputs have not been methodologically corrected or independently rerun as part of this packaging step. See [`IMPLEMENTATION_NOTES.md`](IMPLEMENTATION_NOTES.md) for important scope and reproducibility notes.

## Research overview

MABSA predicts sentiment toward a specific aspect in a post by using both the post text and its associated image. The KE-GCN paper describes three major components:

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
| `IMPLEMENTATION_NOTES.md` | Scope, dataset configuration, and reproducibility caveats. |

## Datasets and external resources

The paper identifies the Twitter-2015 and Twitter-2017 MABSA datasets and points to the following source:

- [TwitterDataMABSA dataset repository](https://github.com/CopotronicRifat/TwitterDataMABSA)
- [ConceptNet](https://github.com/commonsense/conceptnet5/wiki)
- [SenticNet](https://sentic.net/)

The notebooks expect external datasets and preprocessing artifacts. They do **not** include the full Twitter datasets, image files, pretrained model weights, SenticNet files, ConceptNet cache, or all precomputed features. Review the paths near the top of each notebook and configure the required inputs in your environment before running it.

Some notebooks contain Kaggle-specific paths such as `/kaggle/input/piash-dpfn-mabsa-data`. The external dataset directory name is intentionally preserved because it refers to an existing input location, not the GitHub repository name.

## Environment setup

Use Python with a compatible PyTorch installation. For GPU use, install the PyTorch build appropriate for your CUDA environment from the [official PyTorch installation selector](https://pytorch.org/get-started/locally/) before installing the remaining packages.

```bash
pip install -r requirements.txt
```

Open the notebooks in Jupyter or Kaggle. Before execution:

1. Add or download the required dataset and external resources.
2. Update hardcoded input and output paths for your environment.
3. Check that each preprocessing output file matches the path and filename expected by the next notebook.
4. Run the notebooks in the intended preparation-to-training order, checking the notes in `IMPLEMENTATION_NOTES.md`.

## Results reported in the paper

The paper reports the following results:

| Dataset | Accuracy | Macro-F1 |
|---|---:|---:|
| Twitter-2015 | 78.50% | 74.91% |
| Twitter-2017 | 72.37% | 70.22% |

These values are transcribed from the paper and are **not a claim that the supplied notebooks independently reproduce those results**. See the implementation notes for the current notebook scope and evaluation caveats.

## Reproducibility and limitations

This repository is a structured, rebranded copy of the supplied notebooks. It is not a guarantee that the notebooks run end-to-end without environment or artifact adjustments. The current notebook configuration, preprocessing outputs, and evaluation procedure should be checked before using results as an independent reproduction.

No dataset, external resource, or model checkpoint is redistributed here unless it is separately added with appropriate permission.

## Citation

Please cite the associated KE-GCN paper when using this work. See [`CITATION.cff`](CITATION.cff) for the paper title and author metadata.

## License

No license is included at this stage because the appropriate license for the research code and third-party materials has not been confirmed. Add a license only after confirming you have the rights to distribute the code and any included assets.
