# Axiomatic Design Dataset

This repository release an annotated dataset manually curated by two PhD-level researchers with expertise in engineering design.

## Dataset Description

The dataset focuses on the annotation of Axiomatic Design (AXD) elements, specifically Functional Requirements (FRs) and Design Parameters (DPs), as defined in Suh’s Axiomatic Design theory (Suh, 2001).
For further details on the theory, see: https://www.axiomaticdesign.com/technology/axiomatic-design-advances-and-applications/

The dataset consists of 6,000 annotated sentences and it supports the both named entity recognition (NER) and joint entity and relation extraction task (JERE).

### Named Entity Recognition (NER)
As illustrated in Fig. 1, the dataset includes token-level annotations for Axiomatic Design entities:
- **Doer**: The entity required to perform the action described in a FR.
- **Action**: The action of the FR that must be performed by the Doer.
- **Receiver**: The entity affected by the action.
- **Design Parameter (DP)**: A measurable attribute of a component that designers define and adjust within its feasible range to satisfy one or more functional requirements.

### Joint Entity and Relation Extraction (JERE)
As illustrated in Fig. 1, the dataset includes relation annotation between Axiomatic Design NER entity:
- **Doer**: 
- **Receiver**: 
- **Axiomatic**:

![Dataset Overview](https://github.com/MarcoLosanno/axiomatic-design-dataset-JERE_task/blob/main/img/annotation_example_git.svg)

**Fig. 1** - *Example of annotated sentence for NER and JERE task.*

The annotations were conducted using [Doccano](https://doccano.github.io/doccano/), an open-source tool for text annotation that supports both entity and relation labeling.

### Repository Structure

#### `dataset/`
This folder contains the annotated dataset in two formats:
1. **`axiomatic_dataset.xlsx`**: Dataset in Excel format.
2. **`axiomatic_dataset_doccano.jsonl`**: For seamless import into the Doccano annotation tool.

#### `doccano_config/`
This folder includes the JSON configuration file for Doccano, defining:
- **`label_config_entity.json`**: configuration file for entity tags.
- **`label_config_rel.json`**: configuration file for relation tags.

### How to Use
1. Import `axiomatic_dataset_doccano.jsonl`file into [Doccano](https://doccano.github.io/doccano/) for visualization or further annotation.
