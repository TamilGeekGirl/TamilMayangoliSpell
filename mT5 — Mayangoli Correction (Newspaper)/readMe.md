# mT5 — Mayangoli Correction (Newspaper)

## Overview

This module implements the **best-performing model (mT5)** for Mayangoli error correction.

---

## Model

* mT5 (multilingual text-to-text transformer)

---

## Task

Correction of context-sensitive real-word spelling errors in Tamil.

---

## Dataset

* 30,000 sentence pairs
* Generated using linguistically grounded error induction

---

## Pipeline

1. Tamil text preprocessing
2. Error induction using confusion sets
3. Finetuning mT5
4. Evaluation

---


##  Results

* BLEU: **99.28**
* Exact Match Accuracy: **93.50%**

---

##  Notes

* This is the primary model reported in the paper
* Demonstrates strong contextual understanding
