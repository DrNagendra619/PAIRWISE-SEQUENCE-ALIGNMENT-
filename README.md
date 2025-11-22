# PAIRWISE-SEQUENCE-ALIGNMENT-
SEQUENCE ALIGNMENT
# 🧬 Pairwise Sequence Alignment (Global & Local) using BioPython

## 📝 Overview

This Jupyter Notebook demonstrates **Pairwise Sequence Alignment** using the dedicated `Bio.Align` module from the **BioPython** library. It illustrates the fundamental difference between **Global Alignment** (Needleman-Wunsch-like) and **Local Alignment** (Smith-Waterman-like) by applying both methods to sample DNA sequences.

The goal is to find the best possible match between two sequences, quantifying their similarity using a scoring system.

## 🚀 Alignment Concepts and Workflow

The script performs two distinct types of alignment:

### 1. Global Alignment

* **Concept**: Attempts to align the **entire length** of two sequences. It uses an alignment score that penalizes mismatches and gaps throughout the full sequence length, even if a strong local match exists.
* **Sequences**: `SeqA = "GAATCCAG"` and `SeqB = "AACAG"`
* **Settings**: A simple match score (`match_score = 1.0`) is used.
* **Result**: The script calculates the overall alignment score (e.g., `5.0`) and prints the full alignment(s), demonstrating how gaps are introduced to force an end-to-end match.

### 2. Local Alignment

* **Concept**: Finds the **best matching subsequence** within two larger sequences. It focuses on regions of high similarity without penalizing non-matching regions outside the best segment.
* **Sequences**: `Seq1 = "ATTGCGATTAAA"` and `Seq2 = "GCG"`
* **Settings**: The alignment mode is explicitly set to **"local"** (`Align.mode = "local"`).
* **Result**: The script finds and prints the maximum local alignment score (e.g., `3.0`) and outputs the corresponding aligned segment, which typically shows the highest scoring segment of Seq1 aligned against Seq2.

## 🛠️ Requirements

The notebook requires the core **BioPython** library, with a specific focus on the `Bio.Align` module:

```bash
!pip install biopython
