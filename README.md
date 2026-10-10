# Computational Art History

Research portfolio exploring computational art history, machine vision, and critical approaches to AI in visual culture.

## Project 01 — High Renaissance vs. Mannerism

### Research question

To what extent can pretrained vision-language model representations distinguish High Renaissance paintings from Mannerist paintings when evaluated on artists excluded from classifier training?

### Method

This exploratory pilot uses frozen image embeddings from OpenAI's pretrained `openai/clip-vit-base-patch32` model, followed by a logistic regression classifier. The evaluation uses an artist-disjoint split to investigate whether the classifier generalizes beyond the artists represented in training.

### Preliminary results

The current pilot notebook reports:

- **Dataset size:** 320 paintings
- **Training set:** 240 paintings
- **Test set:** 80 paintings
- **Training accuracy:** 99.6%
- **Artist-disjoint test accuracy:** 56.25%

These results are preliminary and require further verification. The difference between training and test accuracy raises questions about generalization. Accuracy alone cannot establish whether the model captures historically meaningful stylistic characteristics.

### Data and reproducibility

The dataset's exact source, image identifiers, label provenance, and licensing conditions must be documented and verified. The Python environment, dependency versions, random seeds, and data-processing steps will also be recorded to support reproducibility.

The notebook is intended to run in Google Colab. Reproduction requires access to the documented data sources and a compatible software environment.

### Limitations and related work

This pilot has a limited sample and tests generalization to a small number of held-out artists. Results may be affected by class balance, artist selection, image quality, historical classification decisions, and dataset composition.

Relevant prior research, including work by Ashton and Boisnard, will be reviewed against the original publications before specific claims or novelty statements are made. The relationship between machine-vision performance and art-historical interpretation requires critical examination.

### Planned next steps

1. Verify dataset provenance, labels, and licensing.
2. Reproduce the pilot in a clean runtime.
3. Audit the artist-disjoint split and evaluation procedure.
4. Record dependency versions and random seeds.
5. Document results, figures, and limitations.
6. Situate the experiment within verified related literature.

**Status:** Exploratory pilot under validation. The current results should not be treated as final research findings.
