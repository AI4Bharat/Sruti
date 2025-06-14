# Recognizing Every Voice: Towards Inclusive ASR for Rural Bhojpuri Women


[![Hugging Face Datasets](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Datasets-blue)](https://huggingface.co/datasets/ai4bharat/Rural_Women_Bhojpuri)
[![arXiv](https://img.shields.io/badge/arXiv-PAPER_ID_HERE-b31b1b.svg)](https://arxiv.org/abs/2506.09653)

This repository contains the resources, dataset information, and code for the Interspeech 2025 paper: "Recognizing Every Voice: Towards Inclusive ASR for Rural Bhojpuri Women." Our work focuses on creating the **SRUTI benchmark** for rural Bhojpuri women and leveraging synthetic speech to improve ASR performance for this underserved demographic.

**Paper Abstract:**
Digital inclusion remains a challenge for marginalized communities, especially rural women in low-resource language regions like Bhojpuri. Voice-based access to agricultural services, financial transactions, government schemes, and healthcare is vital for their empowerment, yet existing ASR systems for this group remain largely untested. To address this gap, we create SRUTI, a benchmark consisting of rural Bhojpuri women speakers. Evaluation of current ASR models on SRUTI shows poor performance due to data scarcity, which is difficult to overcome due to social and cultural barriers that hinder large-scale data collection. To overcome this, we propose generating synthetic speech using just 25–30 seconds of audio per speaker from approximately 100 rural women. Augmenting existing datasets with this synthetic data achieves an improvement of 4.7 WER, providing a scalable, minimally intrusive solution to enhance ASR and promote digital inclusion in low-resource language.

---
## 🔗 Resources

This section provides an overview of and links to the key resources developed and used in this work.

### 📚 Datasets & Text Corpora

* **SRUTI Benchmark Dataset:** For evaluating ASR for rural Bhojpuri women.
    *  🤗 **Link:** [View SRUTI Benchmark](https://huggingface.co/datasets/SakshiJ/Rural_bhojpuri/viewer/default/benchmark)
   *
   * **Objective:** Real-world speech benchmark for rural Bhojpuri women, covering key domains.. 72 minutes, 444 utterances, 51 speakers, 4 target domains
   * **Language:** Bhojpuri (dialect accents from Bhadohi, Jaunpur, Mirzapur districts, UP, India).
   * **Domains:** Agriculture, Health, Government Schemes, Finance, and ice-breaker topics.
   * **Demographics:** Women, 4 age groups (18-60+), varied education.
* **Seed Audio for Synthesis:** 39.4 mins real speech (100 Bhojpuri women, 100 Hindi women).
    *  🤗 **Link:** [View Real Train Data](https://huggingface.co/datasets/SakshiJ/Rural_bhojpuri/viewer/default/train_real)
  * **Objective:** 25-30s speech/100 unique speakers (total 39.4 mins) transcribed.

* **Text Prompts for SRUTI Data Collection:**
    * ➡️ **Access Link:** `[Link]`
* **Text Corpora for Synthetic Data Generation:**
    * Bhojpuri: GPT-4o generated & translated sentences.  ➡️ **Access Link:** `[Link]`

### 🛠️ Tools Used

* **Data Collection and Verification:** [Kathbath app](https://ai4bharat.iitm.ac.in/tools/Kathbath) (Open Source).
* **Data Transcription:** [Shoonya app](https://ai4bharat.iitm.ac.in/tools/Shoonya) (Open Source).

* **Speech Synthesis:** Multilingual prompt-based model [11] (zero-shot for Bhojpuri from Hindi F5]). [IndicF5](https://huggingface.co/spaces/ai4bharat/IndicF5).
* **ASR Architecture:** Conformer-L [17] with Hybrid CTC + RNN-T loss) [IndicConformer](https://github.com/AI4Bharat/IndicConformerASR).

### checkpoint_models Model Checkpoints & Code

* **Code Repository:** Training, evaluation, and synthetic data generation code.
    * Training/Evaluation: 
    * Synthetic Data: 
* **Pre-trained Model Checkpoints (M1-M4):** To be released on GitHub/HF Hub. **[Coming Soon]**

    | Model ID | Description                                       | Datasets Used (Primary additions highlighted)                                                                 | Model Checkpoint Link         |
    | :------- | :------------------------------------------------ | :------------------------------------------------------------------------------------------------------------ | :---------------------------- |
    | **M1** | Monolingual Bhojpuri                              | **Real Bhojpuri (133.4 hrs):** SpeeS-IA [19], ULCA NewsOnAir [6], Vaani [1], LIMMITS [20]                       | [Coming Soon] |
    | **M2** | Bilingual Bhojpuri + Hindi                        | M1 Data + **Real Hindi (376 hrs):** IndicVoices [2]                                                           | [Coming Soon] |
    | **M3** | Bilingual + Synthetic Bhojpuri                  | M2 Data + **Synthetic Bhojpuri (100 hrs)** (Seed: 39.4 mins Bhojpuri women)                                     | [Coming Soon] |
    | **M4** | Bilingual + Synthetic Bhojpuri + Synthetic Hindi | M3 Data + **Synthetic Hindi (100 hrs)** (Seed: ~40 mins Hindi women)                                          | [Coming Soon] |

---


### Data Collection Methodology
1.  **Community Engagement:** Collaboration with ASHA/ANMs for trust and informed consent. 
   *  **Link to Brochure used for engagement:** `[Link]`
3.  **On-Field Collection:** Using **Kathbath app** in government facilities (Primary Health centres (PHCs)).



---
## 🎧 Verification and Transcription

Ensured data quality through rigorous verification and transcription.

### Verification
Verified by in-house experts for clarity and relevance, even with background noise.
   *  **Link to Verification Guidelines Document:** `[Link]`


### Transcription
   *  **Link to Transcription Guidelines Document:** `[Link]`

---
## 🤖 Model Building 

Developed and evaluated ASR models using the SRUTI benchmark and synthetic data.

### Models Trained
*(Refer to the table in "🔗 Resources > checkpoint_models Model Checkpoints & Code" for dataset details.)*
* **M1:** Monolingual Bhojpuri (133.4 hrs real Bhojpuri).
* **M2:** M1 + Real Hindi (376 hrs).
* **M3:** M2 + Synthetic Bhojpuri (100 hrs).
* **M4:** M3 + Synthetic Hindi (100 hrs).

---
## ⚙️ Training and Evaluation Scripts  **[Coming Soon]**

Scripts and configurations for model training and SRUTI benchmark evaluation.

* **Training & Evaluation Scripts:**.
* **Environment Setup:**
    

### Running Experiments


---
## 📜 Citation

If you use the SRUTI dataset, code, or findings from our paper in your research, please cite our work:

```bibtex
@misc{joshi2025recognizingvoiceinclusiveasr,
      title={Recognizing Every Voice: Towards Inclusive ASR for Rural Bhojpuri Women}, 
      author={Sakshi Joshi and Eldho Ittan George and Tahir Javed and Kaushal Bhogale and Nikhil Narasimhan and Mitesh M. Khapra},
      year={2025},
      eprint={2506.09653},
      archivePrefix={arXiv},
      primaryClass={eess.AS},
      url={https://arxiv.org/abs/2506.09653}, 
}
