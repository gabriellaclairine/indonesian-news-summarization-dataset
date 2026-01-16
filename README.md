# Entity and Aspect-Aware Indonesian News Summarization Dataset

## 📌 Overview
This repository contains a manually annotated dataset of **1,000 Indonesian news articles** collected from *Detik.com*. The dataset is designed for abstractive summarization tasks with a focus on **Entity-Aware** and **Aspect-Based** guidance.

## 📂 Dataset Structure
| Column Name | Description |
| :--- | :--- |
| `judul` | The title of the news article. |
| `isi_berita` | The raw text of the article (Input). |
| `summary` | Manually written abstractive summary (Reference). |
| `aspek_target` | The domain category (e.g., Economy, Law, Politics). |
| `entity` | JSON-formatted string containing extracted stakeholders. |

### Entity Categories
Entities are categorized into 5 stakeholder groups:
- **Government** (Pemerintah)
- **Industry** (Industri/Perusahaan)
- **Civil Society** (Masyarakat)
- **Experts** (Pengamat/Ahli)
- **Other** (Lainnya)

### Aspect Categories
The articles are evenly distributed across 5 topics:
1. Economy & Finance
2. Law & Crime
3. Politics & Public Policy
4. Development & Environment
5. Social & Community Affairs

## 📊 Statistics
- **Total Articles:** 1,000
- **Average Article Length:** ~389 words
- **Average Summary Length:** ~42 words
