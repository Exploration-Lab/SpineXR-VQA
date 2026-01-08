3    # SpineXR-VQA: A Clinically-Validated VQA Dataset for Spine X-Rays

[![Paper](https://img.shields.io/badge/Paper-ACM-blue)](INSERT_LINK_HERE) 
[![Dataset](https://img.shields.io/badge/Dataset-HuggingFace-orange)](INSERT_HF_LINK) 
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**SpineXR-VQA** is an open-source, clinically grounded benchmark designed to bridge the gap in spinal musculoskeletal imaging. [cite_start]While Medical VQA has advanced in areas like pneumonia and oncology, spinal imaging remains under-explored[cite: 3, 4]. Our dataset provides high-fidelity, expert-verified reasoning to move beyond simple classification.

## 🌟 Key Features
- [cite_start]**Total Data:** 2,187 X-rays and 8,272 open-ended QA pairs[cite: 5].
- [cite_start]**Expert Verification:** 100% of the dataset was validated by 10 orthopedic specialists from India and Thailand[cite: 7, 19].
- [cite_start]**High Reliability:** Achieved Cohen’s Kappa scores of 0.96 (questions) and 0.93 (answers).
- [cite_start]**Clinical Depth:** Features six reasoning categories: **Abnormality, Severity, Location, Diagnosis, Treatment, and Reasoning**[cite: 6, 21].

## 📊 Dataset Categories & Examples
[cite_start]The dataset focuses on common spinal conditions like disc-space narrowing, fractures, and spondylolisthesis.

| Category | Example Question | Example Answer |
| :--- | :--- | :--- |
| **Abnormality** | What is the nature of the abnormality observed? | [cite_start]The X-ray shows disc space narrowing at the C5-C6 and C6-C7 levels[cite: 485]. |
| **Severity** | Assess the severity of the narrowing. | [cite_start]The narrowing appears moderate, with a noticeable reduction in disc height[cite: 487]. |
| **Reasoning** | What are the possible causes of the narrowing? | [cite_start]Potential causes include age-related wear, trauma, or osteoarthritis[cite: 493]. |

## 🚀 Benchmarking 15 MLLMs
We evaluated 15 state-of-the-art models, including:
- [cite_start]**Proprietary:** GPT-4o, Claude 3.5 Sonnet, Gemini 1.5 Flash[cite: 23, 238].
- [cite_start]**Medical-Specific:** MedGemma, LLaVA-Med, MedFlamingo[cite: 252].
- [cite_start]**General Open-Weight:** LLaVA, DeepSeek-VL, Qwen 2.5[cite: 249, 250].

[cite_start]**Findings:** While models show moderate semantic similarity (median 0.72), they often fail to maintain anatomical fidelity and clinical completeness[cite: 25, 267].

## 🛠️ Getting Started

### Installation
```bash
git clone [https://github.com/Exploration-Lab/SpineXR-VQA.git](https://github.com/Exploration-Lab/SpineXR-VQA.git)
cd SpineXR-VQA
pip install -r requirements.txt
