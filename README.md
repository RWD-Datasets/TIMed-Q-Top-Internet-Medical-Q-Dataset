# TIMed-Q: Top Internet Medical Question Dataset

**TIMed-Q** is a curated dataset of 500 patient-phrased medical questions sourced from real-world internet searches. It is designed to support research in **Large Language Models (LLMs)**, **clinical reasoning**, and **medical safety evaluation** by capturing the authentic language and concerns of patients seeking medical information online.

---

## Dataset Overview

The dataset includes **500 questions**, evenly divided across five clinically relevant domains (100 questions each):

- Symptom Management & Treatment  
- Acute Emergency Scenarios  
- Medication Safety & Drug Interactions  
- Mental Health & Psychiatric Conditions  
- Diagnostic Test & Laboratory Result Interpretation  

Each question preserves the original, natural phrasing as typed by users (e.g.,  
*“I can’t stop worrying do I have anxiety?”*,  
*“Should I go to the ER if my child swallowed a battery?”*),  
enabling models to learn from unfiltered, real-world patient language.

---

## Annotation Information

Each question in TIMed-Q is annotated across the following dimensions:

### Domain Category

Indicates the clinical theme or context of the question:
- Symptom Management & Treatment  
- Acute Emergency Scenarios  
- Medication Safety & Drug Interactions  
- Mental Health & Psychiatric Conditions  
- Diagnostic Test & Laboratory Result Interpretation

### Clinical Area / Diagnosis

Represents the relevant clinical topic or diagnosis:  
Includes both general conditions (e.g., “Abdominal Pain”, “ADHD”, “Borderline Personality Disorder”) and medical specialties.

### Intent Category

Defines the underlying purpose of the question:
- **Symptom Interpretation** – e.g., *“Why do my fingers feel stiff?”*  
- **Diagnosis Interpretation** – e.g., *“My doctor says I have ADHD, what does that mean?”*  
- **Treatment** – e.g., *“How do I treat my spring allergies?”*  
- **Emergency Interpretation** – Based on symptom or event  
- **Test Result Interpretation** – Questions referencing diagnostic test results

---

## Test Result Labels (Diagnosis & Lab/Imaging Test Result Only)

Diagnostic interpretation entries are labeled with explicit test result status:
- Positive  
- Negative  
- Inconclusive  
- Normal  
- Abnormal

---

## Triage Level (Emergency Scenarios Only)

Acute emergency questions are labeled using a five-point triage scale, adapted from ER protocols:

| Level | Description                                           | Examples                                                              |
|-------|-------------------------------------------------------|-----------------------------------------------------------------------|
| 1     | Immediate – Life-saving intervention required         | Cardiac arrest, unresponsive patient, or severe respiratory distress |
| 2     | Emergent – High risk of deterioration                 | Heart attack, stroke                                                  |
| 3     | Urgent – Requires multiple resources (e.g., labs + imaging) | Deep cuts, moderate pain, signs of infection                     |
| 4     | Semi-Urgent – One resource anticipated                | Sprains, minor cuts, earaches                                         |
| 5     | Non-Urgent – Minimal intervention anticipated         | Topical medications, over-the-counter requests                        |

---

## Drug Interaction Categorization (Medication Questions Only)

For medication safety questions, the following metadata is included:

### Interaction Severity
- No Interaction  
- Minor  
- Moderate  
- Severe

### Pharmacological Class
Each drug is mapped to its pharmacological class, such as:
- ACE inhibitor  
- SSRI  
- Beta-blocker  
- NSAID  
- Herbal supplement

---

## File Contents

- `timed_q_dataset.csv`  
