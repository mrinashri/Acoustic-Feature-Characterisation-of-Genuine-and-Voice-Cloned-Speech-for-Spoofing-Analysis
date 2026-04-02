# Acoustic Feature Characterisation of Genuine and Voice Cloned Speech for Spoofing Analysis 🎙️

## 📌 Dataset Preview Repository

This repository provides a **preview of the dataset**.
The preview dataset is available in the file:

**VC_Dataset_Preview.csv**

The **full dataset is available upon request**.

---

## 📊 Dataset Overview

**Dataset Title:** Acoustic Feature Characterisation of Genuine and Voice Cloned Speech for Spoofing Analysis

**Description:**
This work focuses on identifying **low-level acoustic inconsistencies between genuine and synthetic speech** using a structured signal processing pipeline.

The dataset is designed to support **spoofing detection, voice cloning analysis, and acoustic feature research** by providing a structured and interpretable feature representation.

---

## 🧠 System Design and Methodology

### 1️⃣ Dataset Engineering

A key limitation in existing spoof detection research is the lack of realistic datasets.

To overcome this:

* Collected real speech recordings from public figures
* Generated corresponding voice-cloned samples using modern VC systems
* Created a dataset of **11,778 audio segments**
* Each audio segment is **1 second in duration**

**Why 1-second segmentation?**

It enables the detection of **micro-level temporal and spectral anomalies** that are often averaged out in longer audio signals.

---

### 2️⃣ Signal Standardisation and Preprocessing

To ensure consistency across all samples:

* Converted audio to **16 kHz mono WAV format**
* Removed corrupted and silent samples
* Balanced the dataset to avoid classification bias
* Ensured uniform temporal representation

This step eliminates **data-induced variance** and focuses purely on acoustic characteristics.

---

### 3️⃣ Feature Extraction Framework

Each audio segment is transformed into a **69-dimensional feature vector** capturing spectral and temporal dynamics.

#### a) Spectral Envelope Features

**MFCC (20 coefficients)**

* Capture perceptual spectral structure of speech
* Sensitive to formant smoothing in synthetic voices

---

#### b) Temporal Dynamics

**Delta MFCC (20)**
**Delta-Delta MFCC (20)**

* Represent first and second-order temporal derivatives
* Reveal unnatural transitions and lack of micro-modulation

---

#### c) Harmonic Structure

**Chroma STFT**

* Encodes pitch class energy distribution
* Synthetic speech often shows flattened harmonic profiles

---

#### d) Nonlinear Energy Features

**Teager Energy Operator (TEO)**

* Captures instantaneous energy fluctuations
* Genuine speech shows high variability
* Synthetic speech tends to be smoother

---

#### e) Statistical and Spectral Descriptors

* Spectral Centroid → frequency distribution (brightness)
* Spectral Bandwidth → spread of spectral energy
* Spectral Roll-off → high-frequency attenuation
* Zero Crossing Rate → signal noisiness
* RMS Energy → amplitude dynamics

---

## 📁 Feature Representation

* Each row represents **1 second audio segment**
* Each column represents **acoustic feature**
* Stored in structured **CSV format**
* Directly usable for **Machine Learning and Deep Learning pipelines**

---

## 🔍 Observations and Insights

### ✔️ MFCC Analysis

* Genuine speech → high variability in lower coefficients
* Spoofed speech → smoother spectral envelope

### ✔️ Chroma Features

* Genuine speech → dynamic pitch distribution
* Spoofed speech → uniform harmonic energy

### ✔️ TEO Features

* Genuine speech → strong nonlinear energy fluctuations
* Spoofed speech → reduced excitation variability

**Conclusion:**
Synthetic speech lacks **micro-level irregularities inherent in human vocal production**, making acoustic features highly effective for spoofing analysis.

---

## 🎯 Key Takeaways

* Short-duration segmentation improves detection sensitivity
* Acoustic handcrafted features provide strong interpretability
* Lightweight feature representation enables efficient ML/DL usage
* Dataset bridges the gap between lab-generated and real-world spoofing data

---

## 📂 Repository Contents

VC_Dataset_Preview.csv → Sample dataset preview
README.md → Documentation

---

## 📥 Access to Full Dataset

The full dataset is **not publicly available**.

To request access, please send an email to:

**[jmrinashri@gmail.com](mailto:jmrinashri@gmail.com)**

### Include the following:

* Full Name
* Organization / Institution
* Purpose of use
* Research or project details

After review, access to the full dataset will be provided.

---

## 📬 Contact

For dataset access, research collaboration, or queries:

**Email:** [jmrinashri@gmail.com](mailto:jmrinashri@gmail.com)

---

**Preview available | Full dataset on request | Research-focused repository**
