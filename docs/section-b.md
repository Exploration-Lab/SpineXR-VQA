[← Back to Supplementary TOC](../README.md)



---

# Section B — Dataset Structure and Data Fields

**PDF pages:** 3–5 &nbsp;|&nbsp; **See also:** Table 12 &nbsp;|&nbsp; [📥 Download full PDF](../asset/supplementary-material.pdf)

---

Upon acceptance, the cleaned and verified dataset will be released via Hugging Face. The dataset is organized into two main components: (1) CSV files and (2) corresponding image folders.

---

## B.1 CSV Files (Final_csv)

The `Final_csv` directory contains four files corresponding to dataset splits: `India_train`, `India_test`, `Thai_train`, and `Thai_test`.

Each CSV file contains the following fields:

**Table 12 — Description of dataset fields**

| Field Name | Description | Example |
|---|---|---|
| `image_id` | Unique image identifier (file name) | `Vindr_031.png` |
| `category` | Question category (abnormality, severity, location, treatment, reasoning, diagnostic) | `abnormality` |
| `question` | Natural language question | `What abnormality is present?` |
| `answer` | Ground truth answer | `Fracture at L1–L4` |

---

## B.2 Image Folders (Final_images)

The `Final_images` directory contains image data organized by split: `India_train`, `India_test`, `Thai_train`, and `Thai_test`.

Each split includes:

- **`annotated_images/`** — PNG images with clinical annotations
- **`unannotated_images/`** — Raw PNG images without annotations

---

[← Back to Supplementary TOC](../README.md)
