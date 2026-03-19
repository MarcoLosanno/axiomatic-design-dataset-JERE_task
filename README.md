# Axiomatic Design Dataset

This repository release an annotated dataset manually curated by two PhD-level researchers with expertise in engineering design.

## Dataset Description

The dataset focuses on the annotation of Axiomatic Design (AXD) elements, specifically Functional Requirements (FRs) and Design Parameters (DPs), as defined in Suh’s Axiomatic Design theory (Suh, 2001).
For further details on the theory, see: https://www.axiomaticdesign.com/technology/axiomatic-design-advances-and-applications/

The dataset consists of 6,000 annotated sentences and it supports the both named entity recognition (NER) and joint entity and relation extraction task (JERE).

### Named Entity Recognition (NER)
As illustrated in Fig. 1, the dataset includes token-level annotations for Axiomatic Design entities:
- **Doer**: The entity that is required to perform the Action described in a FR.
- **Action**: An action required to be performed by a system, product, or product component.
- **Receiver**: The entity affected by the Action described in a FR.
- **Design Parameter (DP)**: a physical quantity that characterises the design of a system, product, or product component.

### Joint Entity and Relation Extraction (JERE)
As illustrated in Fig. 1, the dataset includes relation annotation between Axiomatic Design NER entity:
- **Doer**: links a Doer to its Action.
- **Receiver**: links an Action to its Receiver.
- **AXR**: links a DP to the Action of the FR which influences.

![Dataset Overview](https://github.com/MarcoLosanno/axiomatic-design-dataset-JERE_task/blob/main/img/annotation_example_git.svg)

**Fig. 1** - *Example of annotated sentence for NER and JERE task.*

The annotations were conducted using [Doccano](https://doccano.github.io/doccano/), an open-source tool for text annotation that supports both entity and relation labeling.

### Repository Structure

#### `dataset/`
This folder contains the annotated dataset in jsonl format:

- **axiomatic_dataset_doccano.jsonl**
  - **Entity tags**: D (Doer), A (Action), R (Receiver), P (Design Parameter)
  - **Relation types**: Doer, Receiver, AXR 

#### `doccano_config/`
This folder includes the JSON configuration file for Doccano, defining:
- **`label_config_entity.json`**: configuration file for entity tags.
- **`label_config_rel.json`**: configuration file for relation tags.

### How to Use
1. Import `axiomatic_dataset_doccano.jsonl`file into [Doccano](https://doccano.github.io/doccano/) for visualization or further annotation.
