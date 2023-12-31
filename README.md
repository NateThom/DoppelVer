# DoppelVer: A Benchmark for Face Verification

![DoppelVer Dataset](Doppelganger_ViSE.png)

## Table of Contents

- [Overview](#overview)
- [Requesting Access](#access)
- [Dataset Details](#dataset-details)
- [Data Description](#data-description)
- [Dataset Structure](#dataset-structure)
- [Usage](#usage)
- [Citation](#citation)
- [License](#license)
- [Code](#code)

## Overview
This repository is intended to provide documentation on the Doppelganger dataset as well as the code that we utilized for collecting, cleaning, pre-processing, and protocol generation. Please note that no data is provided here. A request for the dataset must be submitted as detailed below. 

The **DoppelVer** dataset is a benchmark dataset designed for evaluating and advancing face verification and recognition algorithms. This dataset contains a diverse collection of facial images. The identities depicted were selected in pairs of doppelganger identities. A doppelganger is an identity who is highly visually similar to the source identity, such that they might be mistaken for one another.

This README file provides essential information about the dataset, its structure, and instructions on receiving access and how to use it was intended to be used.

## Access
Individuals interested in using the DoppelVer dataset must submit a request to Dr. Emily Hand at the University of Nevada, Reno. Requests should be sent in email form to emhand@unr.edu and include a signed copy of the end user licence agreement (EULA). The EULA is a file in this github repository.

## Dataset Details

- **Dataset Name**: DoppelVer: A Benchmark for Face Verification
- **Version**: 1.0
- **Release Date**: 10/17/23
- **Number of Subjects**: 390
- **Number of Original Images**: 27,430
- **Number of Pre-Processed Images**: 27,976
- **File Format**: JPG

## Data Description

The DoppelVer dataset includes the following features and attributes:

- Doppelganger pairs: annotation of which identities are doppelgangers to one another.
- Verification Pairs: protocols for evaluating face verification, including paths to two images and a label denoting if the images depict the same of different identities. 

## Dataset Structure

The dataset is organized as follows:
``` bash
DoppelVer/
├── README.md
├── DoppelgangerPairs.csv
├── DoppelgangerProtocol.csv
├── ViSEProtocol.csv
├── Images.zip
├── Images/
│ ├── Original_Images/
│ │ ├── Abigail Spencer/
│ │ │ ├── 00.jpg
│ │ │ ├── 01.jpg
│ │ │ ├── etc.
│ │ ├── etc./
│ │ │ ├── 00.jpg
│ │ │ ├── 01.jpg
│ │ │ ├── etc.
│ ├── CCA_Images/
│ │ ├── Abigail Spencer/
│ │ │ ├── 00_0.jpg
│ │ │ ├── 01_0.jpg
│ │ │ ├── etc.
│ │ ├── etc./
│ │ │ ├── 00_0.jpg
│ │ │ ├── 00_1.jpg
│ │ │ ├── etc.
```
- `DoppelgangerPairs.csv/`: Doppelganger pair annotations.
- `DoppelgangerProtocol.csv/`: One of two protocols. The Doppelganger protocol uses images of a labeled doppelganger pair as negative samples for verification.
- `ViSEProtocol.csv/`: One of two protocols. The ViSE protocol uses images which are identified by a deep model as being highly visually similar.
- `Images.zip/`: A compressed file containing all original images and pre-processed images.
- `Images/`: The resultant directory after decompressing the Images.zip file.
## Usage

Intended use cases are provided in our academic paper, referenced below. DoppelVer is intended to be used for the evaluation of face recognition models. The dataset does not contain sufficient samples, nor diversity to effectively train face recognition models.

## Citation

If you use the DoppelVer dataset in your work, please cite it as:
N. Thom, A. DeBolt, L. Brown, E. M. Hand, “DoppelVer: A Benchmark for Face Verification,” International Symposium on Visual Computing, 2023.

## License

This dataset is provided under our end user licence agreement.

---

We hope you find the DoppelVer dataset valuable for your research or application. If you have any questions or need further assistance, please don't hesitate to contact us at nathanthom@nevada.unr.edu or emhand@unr.edu.
