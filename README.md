
# Computational Art History

**Research portfolio by Zara Nasiruddin**

This repository documents exploratory projects investigating how machine-vision models interpret and classify historical artworks. My work focuses on the use of vision-language models in art history, with particular attention to evaluation, generalisation, and the influence of experimental choices on model outputs.

The projects use CLIP (Contrastive Language–Image Pre-training) to examine two questions: whether visual representations can distinguish High Renaissance from Mannerist paintings when tested on unseen artists, and whether the wording of text prompts affects artwork classification.

These are small-scale experiments intended to explore methodological questions. Their findings are preliminary and should not be treated as definitive conclusions about artistic style or the reliability of AI in art history.

## Projects

### Project 01 — High Renaissance vs. Mannerism

**Question:** Can a classifier using pretrained CLIP image embeddings distinguish High Renaissance from Mannerist paintings when the artists in the test set were excluded from training?

**Method:** Extracted frozen image embeddings using `openai/clip-vit-base-patch32` and trained a logistic regression classifier. The evaluation used an artist-disjoint split to test generalisation beyond the artists represented in training.

**Pilot results:**

- 320 paintings from 16 artists
- 240 paintings for training and 80 for testing
- Training accuracy: 99.6%
- Test accuracy on unseen artists: 56.25%
- Accuracy varied across the four held-out artists.

**Interpretation:** The large difference between training and test performance raises questions about how well the classifier generalises to artists it has not seen. The results do not establish whether the model has learned historically meaningful stylistic characteristics.

**Status:** Exploratory pilot; further validation is needed.

[View the Project 01 notebook](project-01-renaissance-mannerism.ipynb)

---

### Project 02 — CLIP Prompt Robustness in Artwork Classification

**Question:** How much do CLIP's artwork classifications change when the wording of text prompts is altered?

**Method:** Compared multiple prompt formulations using a sample of 40 paintings, balanced between High Renaissance and Mannerism. The experiment examined both broader prompt approaches and more controlled wording variations.

**Main results:**

- Sample: 40 paintings, with 20 per style.
- Broad prompt approaches produced accuracies between 45% and 50%.
- Controlled prompt formulations produced accuracies between 45% and 50%.
- Every image changed its predicted label at least once across the tested prompt conditions.
- Agreement between some prompt formulations was high, while others produced substantially different predictions.

**Interpretation:** The results suggest that classifications in this small experiment were sensitive to prompt wording. They illustrate why prompt design should be treated as an experimental choice rather than a neutral description of an artwork.

**Limitations:** The sample is small, and the results cannot establish how consistently these effects occur across larger collections, other styles, or different models.

**Status:** Completed exploratory experiment; broader validation remains necessary.

[View the Project 02 notebook](project2_clip_prompt_robustness.ipynb)

---

## Methods and tools

- Python
- Google Colab
- PyTorch and Transformers
- CLIP image and text embeddings
- scikit-learn
- Logistic regression and classification evaluation

## Research approach

These projects approach computational art history as a critical investigation of machine-vision methods rather than an attempt to replace art-historical interpretation with automated labels.

The experiments have encouraged further questions about dataset composition, artist-level generalisation, prompt sensitivity, and the difference between a model's classification and a historically grounded interpretation.

## Limitations and reproducibility

Both projects are exploratory. Their findings should be interpreted in relation to their sample sizes, data selection, evaluation procedures, and implementation constraints.

The first project requires further checks of dataset provenance, artist splits, and reproducibility. The second is limited by its small sample and should be extended before drawing broader conclusions.

The notebooks document the experiments and their outputs. Reproduction may require access to the relevant data sources and a compatible software environment.

## About

I have a background in Computer Arts, university-level teaching, and Project Management. I am developing my computational art-history practice through independent experiments with Python and machine vision.

My research interests include digital art history, computer vision, and the ways computational methods shape how historical images are classified, compared, and interpreted.
