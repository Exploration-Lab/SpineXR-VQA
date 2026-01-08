# 🦴SpineXR-VQA: A Clinically-Validated VQA Dataset for Spine X-Rays

[![Paper](https://img.shields.io/badge/Paper-ACM-blue)](INSERT_LINK_HERE) 
[![Dataset](https://img.shields.io/badge/Dataset-HuggingFace-orange)](INSERT_HF_LINK) 
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)


--- 
## 👀 Overview  

SpineXR-VQA is an open-source, clinically grounded **Medical Visual Question Answering (Med-VQA)** benchmark designed to address the under-explored domain of spinal and musculoskeletal imaging. While recent Med-VQA research has advanced clinical decision support in areas such as pneumonia, oncology, and neurology, spine-focused reasoning remains limited due to the lack of domain-specific datasets and realistic evaluation protocols.

The dataset comprises **2,187 spinal X-ray images** paired with **8,272 expert-verified, open-ended question–answer pairs**, curated to reflect the descriptive and diagnostic reasoning used in real-world clinical practice. SpineXR-VQA includes six expert-validated question categories: **abnormality, severity, location, diagnosis, treatment, and  reasoning**.

All annotations were validated by **ten orthopedic specialists from India and Thailand**, ensuring both clinical reliability and geographic diversity, with high inter-rater agreement (Cohen’s Kappa: 0.96 for questions and 0.93 for answers). In addition to dataset curation, SpineXR-VQA provides a comprehensive benchmark of **15 state-of-the-art multimodal large language models (MLLMs)**, revealing persistent challenges in anatomical fidelity and clinical completeness. The dataset is intended to support the development and evaluation of specialized vision–language models for spinal imaging.

Representative examples from the SpineXR-VQA dataset is shown below. 👇


![SpineXR-VQA Examples](asset/SpineXR-VQA(Example).png)


---

## Key Features  

- Spine-specific Med-VQA dataset based on **X-ray radiographs**
- Covers **cervical, thoracic, and lumbar** spine regions
- Clinically grounded question–answer pairs aligned with radiology workflows
- Emphasis on **fracture-related reasoning** and anatomical localization
- Supports benchmarking of **large multimodal language models (MLLMs)**
- Suitable for **evaluation, error analysis, and interpretability studies**

---

## Motivation  

Spinal injuries and degenerative conditions are among the most frequently encountered findings in routine radiological practice. However, existing Med-VQA datasets predominantly focus on chest X-rays, pathology slides, or general anatomical reasoning, offering **limited coverage of spinal imaging**.

SpineXR-VQA is motivated by the need for:
- Domain-specific evaluation of vision–language models on spinal pathology  
- Clinically meaningful questions beyond surface-level visual recognition  
- Safer and more reliable assessment of AI systems for musculoskeletal radiology  

The dataset bridges the gap between **research-centric Med-VQA benchmarks** and **real-world clinical reasoning requirements**.

---

## Dataset Characteristics  

- **Imaging Modality:**  
  - Plain radiographs (X-ray)

- **Anatomical Regions:**  
  - Cervical spine  
  - Thoracic spine  
  - Lumbar spine  

- **Question Types:**  
  - Abnormality detection  
  - Anatomical localization  
  - Attribute description (alignment, deformity, collapse)  
  - Diagnostic interpretation  
  - Clinical reasoning and follow-up implications  

- **Answer Style:**  
  - Concise and clinically grounded  
  - Avoids speculative or unsafe medical claims  

---

## Example of the Dataset  

<!-- Add example image(s) with corresponding question–answer pairs here -->

This section demonstrates how spinal X-ray images are paired with clinically meaningful questions and expert-curated answers.

---

## Abnormalities Covered  

<!-- Add representative abnormality images here -->

SpineXR-VQA primarily focuses on abnormalities relevant to spinal trauma and assessment, including:

- Vertebral fractures  
- Compression deformities  
- Alignment abnormalities  
- Degenerative changes relevant to fracture interpretation  

---

## Benchmarking 15 Multimodal Large Language Models (MLLMs)  

<!-- Add benchmarking table image here -->

SpineXR-VQA has been used to benchmark **15 state-of-the-art multimodal large language models (MLLMs)**, enabling systematic evaluation of:

- Visual grounding accuracy  
- Anatomical localization reliability  
- Diagnostic consistency  
- Hallucination and failure patterns  

---

## Findings  

Key observations from benchmarking and qualitative analysis include:

- Large performance variability across MLLMs for spine-specific tasks  
- Frequent failures in **vertebral-level localization**  
- Confusion between **acute fractures and chronic degenerative changes**  
- Hallucinated findings in the absence of clear visual evidence  

These findings highlight the challenges of applying general-purpose MLLMs to **high-stakes musculoskeletal radiology scenarios**.

---

## Dataset Structure  


Each annotation entry includes:
- Image identifier  
- Question  
- Ground-truth answer  
- Question category (when applicable)

---

## Limitations  

- Limited to **X-ray imaging**; CT and MRI are not included  
- Focuses primarily on **fracture-related reasoning**, not exhaustive spinal pathology  
- Not intended for autonomous clinical diagnosis or treatment decisions  
- Benchmark performance does not imply clinical safety or readiness  

SpineXR-VQA is intended **strictly for research and educational use**.


