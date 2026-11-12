# MedBhasha – Source Declaration

## 1. Dataset Information

- **Dataset Name:** MedBhasha
- **Dataset File:** `annotated_corpus.csv`
- **Total Number of Medical Notes:** 300
- **Total Number of Tokens:** 14,452
- **Annotation Format:** BIO (Beginning, Inside, Outside)
- **Dataset Columns:** `note_id`, `token`, `tag`

## 2. Source and Origin of the Corpus

The entire MedBhasha corpus is a **synthetic dataset generated using Claude AI (Anthropic), Sonnet 5.5**.

The corpus was created in two separate batches:

| Batch | Number of Notes | Source |
|---|---:|---|
| Batch 1 | 150 | Claude AI (Sonnet 5.5) |
| Batch 2 | 150 | Claude AI (Sonnet 5.5) |
| **Total** | **300** | **Fully synthetic, AI-generated** |

Therefore, the complete dataset consists of 300 AI-generated synthetic medical notes (150 + 150 = 300).

No portion of the corpus is declared as an existing real-world patient dataset. The medical notes were generated synthetically for the purpose of creating a medical Named Entity Recognition (NER) corpus.

## 3. Data Characteristics

The dataset contains synthetically generated medical text with annotations for different medical entity categories, including:

- SYMPTOM
- TEST
- TEST_RESULT
- TEMPORAL
- MEDICATION
- DIAGNOSIS
- NEGATION_UNCERTAINTY
- DOSAGE
- BODY_SITE
- PROCEDURE

Each note is represented as a sequence of tokens, with corresponding BIO tags identifying medical entities.

## 4. Data Privacy and External Sources

The corpus was generated as synthetic text rather than collected from real patient records.
No real patient records or personally identifiable patient information were intentionally used in generating the corpus.
No external medical datasets, websites, or third-party documents are declared as source material for the corpus.
The patient details and clinical scenarios represented in the generated notes are fictional and intended for NLP experimentation.

## 5. Annotation and Validation

The generated notes were organized and annotated in BIO format for medical NER.
The annotation data underwent correction and auditing to improve consistency between tokens and their assigned entity tags.
The final corpus contains 300 notes and 14,452 tokens.

## 6. Limitations and Disclaimer

Although the corpus contains medical terminology and clinically structured information, all notes are synthetic and do not represent actual patient encounters.
The generated medical content has not necessarily been clinically verified by qualified medical professionals. Therefore, the dataset is intended for academic research, educational purposes, and NLP experimentation, particularly medical Named Entity Recognition.
It must not be used as a substitute for real clinical data or for medical diagnosis and treatment.

## 7. Final Declaration

We declare that the complete MedBhasha corpus consists of 300 synthetic medical notes generated using Claude AI (Anthropic), Sonnet 5.5.
The dataset was developed in two batches of 150 notes each, giving a total of 300 synthetic notes.

**Final Source Declaration:**

- **Total corpus:** 300 synthetic medical notes
- **First batch:** 150 synthetic notes
- **Second batch:** 150 synthetic notes
- **Generation tool:** Claude AI (Anthropic), Sonnet 5.5
- **Data type:** Fully synthetic
- **Annotation format:** BIO
- **Purpose:** Medical NER research and NLP experimentation

No real-world patient dataset is claimed as the source of any portion of this corpus.
