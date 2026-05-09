# TamilMayangoliSpell: Context-Sensitive Spell Correction for Tamil

##  Overview

This repository contains the implementation of **TamilMayangoliSpell**, a reproducible framework for correcting *Mayangoli errors* in Tamil. This repository accompanies a research paper accepted for presentation at the ACL DravidianLangTech 2026 Workshop, to be held on July 3, 2026.

Mayangoli errors are context-sensitive real-word errors arising from confusion among phonetically similar graphemes such as:

* ல / ள / ழ
* ர / ற
* ந / ன / ண

Since both incorrect and correct forms are valid words, dictionary-based spell checkers fail, requiring **context-aware modelling**.

---

## Contributions

This work introduces:

1. **Tamil-specific preprocessing**

   * Sentence segmentation
   * Text normalization

2. **Linguistically grounded error induction**

   * Controlled corruption based on grapheme confusion sets
   * Ensures dictionary-valid outputs

3. **Model finetuning framework**

   * mBART
   * mT5
   * NLLB

---
##  Overall pipeline
<img width="667" height="735" alt="image" src="https://github.com/user-attachments/assets/12ee6d15-1d9c-4a1f-864b-1b79b196134a" />


---

## Dataset

* Source: *TamilCorp*
* Size: **30,000 sentence pairs**
* Split:

  * Train: 80%
  * Validation: 10%
  * Test: 10%

---

##  Models Evaluated

* mBART
* mT5
* NLLB

---

##  Decoding Settings

* Beam search: **5**
* Max length: **128**

---

## Results

| Model | BLEU      | Exact Match Accuracy |
| ----- | --------- | -------------------- |
| mT5   | **99.28** | **93.50%**           |
| mBART | 92.98     | 89.53                |
| NLLB  | 94.73     | 0                    |

**mT5** performs best and generalizes well to cross-genre evaluation (short stories).

---

##  Repository Structure

* `mbart_newspaper/` — mBART experiments (newspaper)
* `mt5_newspaper/` — mT5 experiments (newspaper)
* `nllb_newspaper/` — NLLB experiments (newspaper)
* `mt5_shortstories/` — cross-genre evaluation (short stories)
* `Preprocessing scripts/` — all the modules needed for abbreviation normalisation, chunk based ingestion, valid mayangoli error induction 
* `screenshots_cli_gui/` — execution evidence

---

## Reproducibility

Each folder contains:

* Training scripts
* Evaluation pipeline
* Configuration details

---

## Notes

* Datasets are not redistributed; instructions provided per module
* Model checkpoints are not included due to size constraints

---

##  Created and maintained by Dr.Yazhmozhi (PhD)

This repository accompanies a research paper accepted for presentation at the ACL DravidianLangTech 2026 Workshop, to be held on July 3, 2026.
