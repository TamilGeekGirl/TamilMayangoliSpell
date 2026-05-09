# Preprocessing Scripts

This folder contains preprocessing utilities used in **TamilMayangoliSpell** to prepare raw Tamil text for Mayangoli error induction and model training.

## Purpose

The preprocessing pipeline converts raw Tamil corpus text into clean, sentence-level data suitable for generating context-sensitive real-word Mayangoli error–correction pairs.

The scripts handle:

- Tamil text cleaning
- whitespace normalisation
- abbreviation handling
- sentence segmentation
- removal of non-Tamil symbols where required
- preparation of clean sentences for error induction

## Pipeline Overview

The preprocessing stage follows these steps:

1. **Input raw Tamil text**
2. **Normalise abbreviations**  
   Common abbreviations are expanded or handled before sentence splitting to reduce incorrect boundary detection.
3. **Clean text**
   - remove unwanted symbols
   - normalise spacing
   - retain Tamil text content
4. **Segment into sentences**
5. **Export cleaned sentence-level data**

The cleaned sentences are then used by the error induction scripts to generate parallel pairs of the form:

```text
<sentence with Mayangoli error, correct sentence>
