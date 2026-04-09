[← Back to Supplementary TOC](../SUPPLEMENTARY_README.md)

---

# Section H — Model Output Error Analysis

**PDF pages:** 40–49 &nbsp;|&nbsp; **See also:** Table 17 &nbsp;|&nbsp; [📥 Download full PDF](../asset/supplementary-material.pdf)

---

This section presents a fine-grained qualitative analysis of clinically relevant failure cases observed across the five representative models evaluated in the main text. For each model, we report selected question–answer examples covering abnormality detection, anatomical localization, diagnostic interpretation, and management reasoning, with clinically incorrect or misleading phrases explicitly highlighted. The examples reveal consistent failure patterns, including false-negative findings in the presence of fractures, substitution of acute traumatic pathology with chronic degenerative conditions, anatomically implausible localization across spinal regions, and unsafe or incomplete treatment recommendations. By directly contrasting model-generated responses with expert-validated ground truth, this analysis demonstrates how high semantic similarity scores can obscure clinically critical errors, underscoring the need for clinician-centered evaluation beyond surface-level text similarity in medical VQA systems.

---

## Table 17 — Representative Clinical Failure Cases

 > ⚠️ **Note:** Clinically incorrect or misleading phrases are marked in **bold** in the Model Output column below.

---

### BLIP-2

| Question | Ground Truth (Clinician) | Model Output | Error Type |
|---|---|---|---|
| Can you identify the radiographic abnormality present in the X-ray image? | Comminuted fracture of the C5 vertebra with vertebral body collapse and posterior element involvement. | The most likely clinical interpretation is ***degenerative disc disease characterized by osteophytes and disc space narrowing***. | Pathology substitution |
| Can you identify the specific areas within the image that show abnormalities? | Abnormalities are located in the lumbar spine at the L4–L5 and L5–S1 levels. | The abnormalities are located at the ***C5–C6 and C6–C7*** levels. | Anatomical mislocalization |
| Does this image reveal any pathological features? | Yes. The image shows a compression fracture of the C6 vertebra. | ***No pathological features detected***. | False-negative detection |
| Given the X-ray image, what is the most probable clinical interpretation? | Lumbar spine fracture at L1 with vertebral body displacement. | The most likely clinical interpretation is ***degenerative disc disease with osteophyte formation***. | Reasoning collapse |
| Can you identify the anatomical site of the fracture depicted in the image? | Fracture located at the C6 vertebra in the cervical spine. | The anatomical site of the fracture is the ***junction between C5 and C6***. | Anatomical inaccuracy |
| Does this image reveal any pathological features? | Yes. The image shows a fracture of the right clavicle. | ***No pathological features detected***. | Missed extra-spinal pathology |

---

### Claude Sonnet

| Question | Ground Truth (Clinician) | Model Output | Error Type |
|---|---|---|---|
| Can you identify the radiographic abnormality present in the X-ray image? | Compression fracture of the C5 vertebra with vertebral body collapse. | The most likely clinical interpretation is ***degenerative disc disease characterized by osteophytes***. | Pathology substitution |
| Can you identify the specific areas within the image that show abnormalities? | Abnormalities are located in the lumbar spine at the L4–L5 and L5–S1 levels. | The abnormalities are located at the ***C5–C6 and C6–C7*** levels. | Anatomical mislocalization |
| Does this image reveal any pathological features? | Yes. The image shows a compression fracture of the C6 vertebra. | ***No pathological features detected.*** | False-negative detection |
| Given the X-ray image, what is the most probable clinical interpretation? | Lumbar spine fracture at L1 with vertebral body displacement. | The most likely clinical interpretation is ***degenerative disc disease with osteophyte formation***. | Reasoning collapse |
| Can you identify the anatomical site of the fracture depicted in the image? | Fracture located at the C6 vertebra in the cervical spine. | The anatomical site of the fracture is the ***junction between C5 and C6***. | Anatomical inaccuracy |
| Does this image reveal any pathological features? | Yes. The image shows a fracture of the right clavicle. | ***No pathological features detected.*** | Missed extra-spinal pathology |

---

### DeepSeek-VL2

| Question | Ground Truth (Clinician) | Model Output | Error Type |
|---|---|---|---|
| Can you identify the radiographic abnormality present in the X-ray image? | Compression fracture of the C6 vertebra with vertebral body collapse. | The image most likely represents ***degenerative disc disease with osteophyte formation***. | Pathology substitution |
| Does this image reveal any pathological features? | Yes. The image shows a comminuted fracture of the C5 vertebra. | ***No pathological features detected.*** | False-negative detection |
| Can you identify the specific areas within the image that show abnormalities? | Abnormalities are present in the lumbar spine at the L1–L2 and L2–L3 levels. | The abnormalities are located at the ***C5–C6 and C6–C7*** levels. | Anatomical mislocalization |
| Given the X-ray image, what is the most probable clinical interpretation? | Lumbar vertebral compression fracture with displacement. | The most likely clinical interpretation is ***degenerative disc disease***. | Reasoning collapse |
| Can you identify the anatomical site of the fracture depicted in the image? | Fracture located at the L1 vertebra in the lumbar spine. | The fracture is located in the ***cervical spine at C5–C6***. | Anatomical inaccuracy |
| Given the presence of detected abnormalities, what treatment or management strategies are recommended? | Immediate spinal immobilization with urgent surgical consultation. | ***Conservative management with physiotherapy and lifestyle modification***. | Unsafe management suggestion |

---

### LingShu-7B (zero-shot)

| Question | Ground Truth (Clinician) | Model Output | Error Type |
|---|---|---|---|
| Can you identify the radiographic abnormality present in the X-ray image? | Comminuted fracture of the C5 vertebra with vertebral body collapse. | The findings are consistent with ***degenerative disc disease with osteophyte formation***. | Pathology substitution |
| Does this image reveal any pathological features? | Yes. The image shows a compression fracture of the C6 vertebra. | ***No pathological features detected.*** | False-negative detection |
| Can you identify the specific areas within the image that show abnormalities? | Abnormalities are located in the lumbar spine at the L4–L5 and L5–S1 levels. | The abnormalities are present at the ***C5–C6 and C6–C7*** levels. | Anatomical mislocalization |
| Given the X-ray image, what is the most probable clinical interpretation? | Lumbar spine fracture at L1 with vertebral body displacement. | The most likely clinical interpretation is ***degenerative disc disease***. | Reasoning collapse |
| Can you identify the anatomical site of the fracture depicted in the image? | Fracture located at the C6 vertebra in the cervical spine. | The fracture is located at the ***junction between C5 and C6***. | Anatomical inaccuracy |
| Given the presence of detected abnormalities, what treatment or management strategies are recommended? | Urgent spinal immobilization and surgical consultation are required. | ***Conservative management with physiotherapy and pain control***. | Unsafe management recommendation |

---

### MedGemma (fine-tuned)

| Question | Ground Truth (Clinician) | Model Output | Error Type |
|---|---|---|---|
| Can you identify the radiographic abnormality present in the X-ray image? | Compression fracture of the C6 vertebra with loss of vertebral body height. | The findings are most consistent with ***degenerative disc disease characterized by osteophytes***. | Pathology substitution |
| Does this image reveal any pathological features? | Yes. The image shows a fracture of the right clavicle. | ***No pathological features detected.*** | Missed extra-spinal pathology |
| Can you identify the specific areas within the image that show abnormalities? | Abnormalities are located in the lumbar spine at the L4–L5 and L5–S1 levels. | The abnormalities are identified at the ***C5–C6 and C6–C7*** levels. | Anatomical mislocalization |
| Given the X-ray image, what is the most probable clinical interpretation? | Lumbar spine fracture at L1 with vertebral body displacement. | The most likely clinical interpretation is ***degenerative disc disease with disc space narrowing***. | Reasoning collapse |
| Can you identify the anatomical site of the fracture depicted in the image? | Fracture located at the L1 vertebra in the lumbar spine. | The fracture is located in the ***cervical spine at C5–C6***. | Anatomical inaccuracy |
| Given the presence of detected abnormalities, what treatment or management strategies are recommended? | Immediate spinal immobilization with urgent surgical evaluation. | ***Conservative treatment with physiotherapy and lifestyle modification***. | Unsafe management recommendation |

---

[← Back to Supplementary TOC](../SUPPLEMENTARY_README.md)
