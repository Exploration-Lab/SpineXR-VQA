[← Back to Supplementary TOC](../SUPPLEMENTARY_README.md)

---

# Section C — Train and Test Set Examples

**PDF pages:** 5, 46–47 &nbsp;|&nbsp; **See also:** Tables 13 & 14 &nbsp;|&nbsp; [📥 Download full PDF](../asset/supplementary-material.pdf)

---

Tables 13 and 14 present representative question–answer examples from the training and test splits of **SpineXR-VQA**. The examples illustrate the diversity of clinical reasoning captured by the dataset, ranging from abnormality detection in normal radiographs to multi-step interpretation involving severity assessment, anatomical localization, diagnostic inference, and treatment planning in abnormal cases. Notably, the test-set examples demonstrate greater linguistic and clinical variability, reflecting the use of distinct prompt templates for train and test splits and reinforcing the dataset's focus on evaluating generalization rather than memorization.

---

## Table 13 — Sample Question–Answer Pairs for Train Set

**Example 1: Image ID — `vindr_train_4473.png`**

| Category | Question | Answer |
|---|---|---|
| Abnormality | Is there any abnormality present in this image? | No abnormality detected. |

---

**Example 2: Image ID — `vindr_train_2027.png`**

| Category | Question | Answer |
|---|---|---|
| Abnormality | Is there any abnormality present in this image? | Yes, there is an abnormality present in this image. The X-ray shows a compression fracture of the L1 vertebra with evidence of callus formation, indicating a healing process. |
| Severity | What is the severity of the fracture? | The fracture is of moderate severity. It appears stable without significant displacement, although vertebral body compression may contribute to spinal stenosis. |
| Location | Where is the fracture located in the image? | The fracture is located at the L1 vertebra, just below the T12–L1 disc space, in the midline of the lumbar spine. |
| Diagnostic | What is the most likely diagnosis based on the X-ray image? | The most likely diagnosis is a compression fracture of the L1 vertebra, likely due to osteoporosis or trauma. |
| Reasoning | What are the possible causes of the fracture? | Possible causes include osteoporosis-related bone weakening or traumatic injury such as a fall or accident. |
| Treatment | What is the suggested treatment or management option for the detected abnormalities? | Conservative management including rest, pain control, and physical therapy is recommended, with surgical intervention considered in severe or unstable cases. |

---

**Example 3: Image ID — `vindr_train_2530.png`**

| Category | Question | Answer |
|---|---|---|
| Abnormality | Is there any abnormality present in this image? | Yes, the image shows a compression fracture of the L1 vertebra with vertebral body height loss. |
| Severity | What is the severity of the fracture? | The fracture is of moderate severity and appears stable without rotational displacement. |
| Location | Where is the fracture located in the image? | The fracture involves the anterior aspect of the L1 vertebral body in the lumbar spine. |
| Diagnostic | What is the most likely diagnosis for the fracture? | A healing compression fracture of the L1 vertebra, potentially associated with osteoporosis or trauma. |
| Reasoning | What are the possible causes of the fracture? | Osteoporosis, traumatic injury, metabolic bone disease, or long-term medication use affecting bone density. |
| Treatment | What is the suggested treatment or management option for the fracture? | Conservative management including rest, analgesia, physical therapy, and possible bracing, with surgery reserved for unstable cases. |

---

## Table 14 — Sample Question–Answer Pairs for Test Set

**Example 1: Image ID — `vindr_test_1251.png`**

| Category | Question | Answer |
|---|---|---|
| Abnormality | Does this image reveal any pathological features? | No abnormality detected. |

---

**Example 2: Image ID — `vindr_test_538.png`**

| Category | Question | Answer |
|---|---|---|
| Abnormality | Can the X-ray image be evaluated for any radiographic abnormalities? | The X-ray image shows multiple abnormalities, including vertebral collapse, osteophyte formation, and the presence of a surgical implant. |
| Severity | Assess the degree of vertebral compression. | The vertebral collapse appears moderate to severe, with significant loss of vertebral height and potential compromise of spinal stability. |
| Location | Can you identify the specific areas within the image that show abnormalities? | The abnormalities are located in the lumbar spine, primarily at the L1–L2 and L2–L3 levels. |
| Diagnostic | Given the X-ray image, what is the most probable clinical interpretation? | The most likely diagnosis is degenerative disc disease with vertebral collapse and osteophyte formation, possibly complicated by prior surgical intervention. |
| Reasoning | Identify the underlying factors contributing to the observed abnormalities. | Potential contributing factors include degenerative disc disease, osteoporosis, prior trauma, or infection. |
| Treatment | Given the presence of detected abnormalities, what treatment or management strategies are typically recommended? | Recommended management includes conservative treatment with analgesics and physical therapy, surgical stabilization if indicated, and regular follow-up to monitor disease progression. |

---

**Example 3: Image ID — `vindr_test_277.png`**

| Category | Question | Answer |
|---|---|---|
| Abnormality | Does this image reveal any pathological features? | Yes, the image demonstrates a compression fracture involving the C6 vertebra. |
| Severity | Assess the fracture's degree of displacement and comminution to determine its overall severity. | The fracture is of moderate severity, with partial compression and potential cervical spine instability but no complete displacement. |
| Location | Can you identify the anatomical site of the fracture depicted in the image? | The fracture is located at the C6 vertebra in the mid-cervical spine, approximately between the C5 and C7 levels. |
| Diagnostic | Given the X-ray image, what is the most probable clinical interpretation? | The most likely diagnosis is a compression fracture of the C6 vertebra. |
| Reasoning | Identify the underlying factors that may have contributed to the fracture. | Possible causes include traumatic injury, osteoporosis, or other conditions that weaken vertebral bone integrity. |
| Treatment | Given the presence of detected abnormalities, what are the recommended treatment or management strategies? | Management typically involves cervical spine immobilization using a collar or halo vest, followed by rehabilitation; surgical stabilization may be required in severe cases. |

---
