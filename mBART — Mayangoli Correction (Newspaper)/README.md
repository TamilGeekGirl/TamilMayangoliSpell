# mBART — Mayangoli Correction (Newspaper)

## Overview

This module implements Mayangoli error correction using **mBART** on newspaper-domain Tamil text.

---

## Model

* mBART (multilingual sequence-to-sequence)

---

## Task

Context-sensitive correction of real-word Tamil spelling errors.

---

## Data

* Derived from TamilCorp
* Error-induced sentence pairs using grapheme confusion rules

---

## Pipeline

1. Preprocessing (normalization + segmentation)
2. Error induction
3. Finetuning mBART
4. Evaluation

