# 🩺 MedBhasha --- Bengali Clinical NLP & Intelligent Medical Information Retrieval

```{=html}
<p align="center">
```
**Team Train Test Panic \| COMSYS Hackathon 8 --- Round 2**
```{=html}
</p>
```
```{=html}
<p align="center">
```
*Bridging the gap between Bengali clinical narratives and structured
medical intelligence.*
```{=html}
</p>
```

------------------------------------------------------------------------

## 01 · The Challenge

Clinical information is often recorded in unstructured language. In
Bengali healthcare settings, extracting meaningful medical information
from clinical notes presents additional challenges involving language
variation, medical terminology, entity boundaries, and contextual
meaning.

**MedBhasha** addresses this problem through an integrated Bengali
Clinical NLP pipeline that transforms unstructured clinical narratives
into structured medical entities, discovers patterns across patient
notes, and retrieves evidence relevant to natural-language clinical
queries.

## 02 · What We Built

The project brings together four connected components:

-   **Clinical Named Entity Recognition (NER):** Identifies and
    classifies clinically meaningful entities across ten predefined
    categories.
-   **Clinical Note Clustering:** Groups notes using extracted clinical
    information to discover similarities and patterns.
-   **Entity & Relationship Analysis:** Examines entity distributions,
    frequencies, and co-occurrence patterns.
-   **Retrieval-Augmented Generation (RAG):** Retrieves relevant
    evidence from the team's annotated corpus and generates
    query-oriented responses.

## 03 · System Architecture

``` mermaid
flowchart TD
    A["Annotated Bengali Clinical Corpus"] --> B["Text Processing & Tokenization"]
    B --> C["Clinical NER"]
    C --> D["Structured Entity Extraction"]
    D --> E["Clinical Note Clustering"]
    D --> F["Entity Frequency & Relationship Analysis"]
    A --> G["Corpus-Based Retrieval Index"]
    G --> H["Bengali Clinical Query"]
    H --> I["Evidence Retrieval"]
    I --> J["Grounded Response & Evidence"]
    C --> K["NER Evaluation"]
    E --> L["Clustering Evaluation"]
```

## 04 · Clinical Entity Schema

The NER pipeline recognizes ten clinical entity categories:

  Entity                   Description
  ------------------------ ---------------------------------------
  `DIAGNOSIS`              Diagnosed medical conditions
  `SYMPTOM`                Patient-reported or observed symptoms
  `MEDICATION`             Medicines and drugs
  `DOSAGE`                 Medication dosage and quantities
  `TEST`                   Medical investigations and tests
  `TEST_RESULT`            Findings and measured results
  `BODY_SITE`              Anatomical locations
  `PROCEDURE`              Medical procedures
  `TEMPORAL`               Dates, durations, and time references
  `NEGATION_UNCERTAINTY`   Negation and uncertainty expressions

The annotated corpus uses the BIO tagging scheme:

-   `B-ENTITY`: Beginning of an entity
-   `I-ENTITY`: Continuation of an entity
-   `O`: Token outside an entity

## 05 · Evaluation Framework

The pipeline is evaluated at multiple levels.

  -----------------------------------------------------------------------
  Component                           Evaluation
  ----------------------------------- -----------------------------------
  NER                                 Entity-level Precision, Recall and
                                      F1-score

  Clustering                          Normalized Mutual Information (NMI)
                                      and Adjusted Rand Index (ARI)

  Retrieval                           Evidence relevance, concept
                                      coverage and retrieval quality

  RAG                                 Grounding, answer relevance and
                                      evidence traceability
  -----------------------------------------------------------------------

Evaluation scores and final results should be reported from actual Round
2 execution outputs, not estimated from training performance.

## 06 · Repository Structure

``` text
Train-Test-Panic-MedBhasha/
│
├── round 1/
│   ├── annotated_corpus.csv
│   ├── validation_report.md
│   └── source_declaration.txt
│   └── EDA_summary.pdf
│   └── raw_data.csv
│
├── resources/
│   ├── annotation_guidelines.pdf
│   ├── medbhasha_bengali_clinical_notes(test data).csv
│   ├── test_queries_bn.csv
│   └── validate.py
│
├── notebooks/
│   └── final_notebook.ipynb
│
├── predictions/
│   ├── ner_predictions.csv
│   ├── clusters.csv
│   ├── rag_outputs.jsonl
│   └── analysis/
│
├── requirements.txt
├── REPORT.md
└── README.md
```

## 07 · Getting Started

### Prerequisites

-   Python 3.10+
-   Jupyter Notebook or Google Colab
-   GPU recommended for transformer-based NER training

### Installation

``` bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_REPOSITORY_FOLDER>

pip install -r requirements.txt
```

### Data Preparation

Place the required CSV files in `data/`:

-   Annotated corpus for model training.
-   Hidden test notes for inference and clustering.
-   Bengali clinical queries for retrieval and question answering.

Keep hidden test data separate from the annotated training corpus. The
RAG retrieval index must be constructed exclusively from the team's own
annotated corpus. Do not commit private or competition-restricted test
data to a public repository.

### Run the Pipeline

1.  Open `notebooks/final_notebook.ipynb`.
2.  Execute the notebook from beginning to end.
3.  Verify the generated prediction and analysis files in
    `predictions/`.

## 08 · Output Artefacts

  Output                  Purpose
  ----------------------- -------------------------------------------------------
  `ner_predictions.csv`   Predicted clinical entities and their labels
  `clusters.csv`          Cluster assignments for clinical notes
  `rag_outputs.jsonl`     Query responses with retrieved evidence
  `analysis/`             Entity statistics, relationships and cluster analysis

Round 1 documentation and data provenance are retained in `round1/`.

## 09 · Responsible Use & Limitations

MedBhasha is a hackathon research prototype, not a clinically validated
diagnostic system.

-   Extracted entities and generated responses may contain errors.
-   Retrieval relevance does not establish clinical correctness.
-   Dataset coverage and annotation quality influence model performance.
-   Clinical deployment would require expert validation, privacy
    safeguards, and further evaluation.

## 10 · Team

**Train Test Panic**

COMSYS Hackathon 8 --- MedBhasha Round 2

------------------------------------------------------------------------

*Built to explore structured clinical intelligence from Bengali medical
narratives.*
