# ece6143-project  
# Jet Tagging with CNN and ResNet50 Fine-Tuning

This project performs **jet tagging** using deep learning, focusing on distinguishing **signal** vs **background** jets from particle physics data.  
The work includes full preprocessing, jet image construction, CNN modeling, and ResNet50 transfer learning.  
All results are based on running code inside Google Colab.

---

##  Project Overview

High-energy physics experiments produce jets—collimated sprays of particles.  
Identifying whether a jet originates from a **top quark (signal)** or **QCD background** is a key task in jet tagging.

This project builds two models:

1. **CNN (from scratch)** — trained on custom 33×33 jet images  
2. **ResNet50 (ImageNet fine-tuning)** — using upsampled 75×75×3 images

Both models are trained and evaluated on the same dataset and compared using accuracy and ROC–AUC.

---

##  Dataset

The dataset `val.h5` is downloaded from Zenodo:  
https://zenodo.org/records/2603256/files/val.h5

We use:

- **Signal**: Top-quark jets (10,000 events)  
- **Background**: QCD jets (10,000 events)

Each event contains 200 particles with (E, px, py, pz), and the leading fat jet is reconstructed using the anti-kT algorithm.

