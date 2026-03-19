# Multiple-Sequence-Alignment-Analysis-with-Biopython-HIV-p6-Protein-
Python-based analysis of multiple sequence alignments using Biopython, including gap filtering, consensus generation, epitope analysis, and sequence similarity classification.


## Multiple Sequence Alignment Analysis with Biopython (HIV p6 Protein)

This project implements a set of Python scripts to analyze a multiple sequence alignment (MSA) of HIV p6 protein sequences using Biopython. The workflow performs alignment preprocessing, consensus sequence generation, epitope analysis, and sequence similarity-based classification.

---

## Project Overview

The HIV p6 protein is highly variable and plays a role in viral pathogenicity. This project analyzes an MSA of p6 sequences to extract biologically meaningful insights using computational methods.

---

## Objectives

- Remove highly gapped regions from an alignment  
- Compute consensus sequences  
- Quantify epitope presence across sequences  
- Identify most similar sequences using distance metrics  
- Classify sequences based on subtype similarity  

---

## Scripts

- `compress-gaps.py`  
  - Removes alignment positions where ≥67% of sequences contain gaps  
  - Produces a filtered MSA for downstream analysis  

- `print-consensus.py`  
  - Computes the consensus sequence across all alignment positions  
  - Selects the most frequent amino acid per site  

- `epitope-fraction.py`  
  - Calculates the fraction of sequences containing a given epitope  
  - Treats gaps as mismatches  

- `closest-sequences.py`  
  - Identifies the top 3 most similar sequences to a query  
  - Uses Hamming distance as similarity metric  

- `get-subtype.py`  
  - Predicts subtype of an input sequence  
  - Computes average distance to sequences grouped by subtype  
  - Assigns subtype with smallest average distance  

---

## Methodology

### Alignment Processing

- Reads FASTA-formatted MSA  
- Filters columns based on gap frequency  
- Preserves sequence integrity after filtering  

---

### Consensus Calculation

- Evaluates each alignment position  
- Selects most frequent amino acid (including gaps if present)  

---

### Epitope Analysis

- Searches for exact subsequence matches  
- Computes proportion of sequences containing the epitope  

---

### Sequence Similarity

- Uses Hamming distance to compare sequences  
- Ranks sequences by similarity to input query  

---

### Subtype Classification

- Extracts subtype from sequence identifiers  
- Computes average distance between query and subtype groups  
- Assigns subtype with minimum average distance  

---

## Technologies Used

- Python  
- Biopython  
- NumPy  

---

## Input

- Multiple sequence alignment in FASTA format  
- Query sequences and epitopes provided via command-line arguments  

---

## Output

- Filtered MSA files  
- Consensus sequence  
- Epitope frequency values  
- Ranked similar sequences  
- Predicted subtype classifications  

---

## Key Features

- Automated MSA preprocessing  
- Consensus sequence generation  
- Epitope-level analysis  
- Sequence similarity ranking  
- Subtype classification based on distance metrics  

---

## Key Skills Demonstrated

- Sequence analysis and bioinformatics workflows  
- Multiple sequence alignment processing  
- String and sequence manipulation  
- Distance-based similarity metrics  
- Classification using biological metadata  
- Python scripting with Biopython  

---

## Notes

- Gap characters are treated as mismatches in comparisons  
- Hamming distance assumes equal-length aligned sequences  
- Subtype classification is based on a simple distance-based heuristic  

---


## Author

Lakshita Arunkumar
