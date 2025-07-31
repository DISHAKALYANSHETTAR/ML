
##  **Project Title:**

**Vision-Aided Intelligence with Visual Question Answering for Medical Imaging**

---

##  **What is the project about?**

This project is an **AI-based healthcare solution** that answers natural language clinical questions based on **retinal fundus images** to support doctors in diagnosing **Diabetic Macular Edema (DME)**. It uses **Visual Question Answering (VQA)**—a machine learning technique combining image processing and natural language understanding.

---

##  **Motivation / Problem Statement:**

* In medical imaging, radiologists and ophthalmologists often need **quick and accurate interpretation** of images along with answers to specific questions.
* Manual diagnosis of DME is time-consuming and subjective. There's a need for **AI tools** that can provide **consistent, accurate, and explainable** outputs.
* Our system allows medical professionals to simply **ask questions like "Are there hard exudates in the macula?"** and get **precise answers** from the model based on image analysis.

---

##  **Core Technologies Used:**

| Component                         | Purpose                                                                       |
| --------------------------------- | ----------------------------------------------------------------------------- |
| **VGG16**                         | Extracts deep visual features from retinal images                             |
| **Word2Vec**                      | Converts clinical questions into numerical vectors capturing semantic meaning |
| **LSTM (Long Short-Term Memory)** | Understands the sequence and context of words in the question                 |
| **Late Fusion Technique**         | Merges image and text features for final decision-making                      |

---

## 🛠 **How It Works (Workflow Overview):**

1. **Image and question are inputs** to the system.
2. **Preprocessing:**

   * Images resized to retain medical detail (448x448 pixels).
   * Questions are cleaned, tokenized, and embedded using Word2Vec.
3. **Feature Extraction:**

   * VGG16 captures visual patterns like hard exudates.
   * LSTM understands the context of the medical question.
4. **Fusion:**

   * Features from both inputs are concatenated.
5. **Prediction:**

   * Final classification layer predicts the answer using Softmax.

---

##  **Results Achieved:**

* **Training Accuracy:** 96.88%
* **Validation Accuracy:** 87.52%
* Outperformed **ResNet101**, a deeper model, because VGG16 captured high-level domain-specific features more effectively for DME grading.

---

##  **Key Innovations:**

* Unlike rule-based systems, this model **learns to answer both direct and related questions** consistently (e.g., about different retinal regions).
* Despite being a lightweight multimodal fusion model, it showed **high accuracy and interpretability**, important for medical domains.
* Demonstrated the ability to handle **semantic and regional context**, which is critical in DME assessment.

---

##  **Dataset Used:**

* Combined images from **IDRiD and e-Ophta** datasets.
* Total of **\~679 images** and **13,470+ question-answer pairs**.
* Covered various types of questions:

  * Overall DME grade
  * Presence of hard exudates in image/macula
  * Region-based analysis

---

## ⚙ **Performance Evaluation:**

* Consistency was tested by comparing the model’s answers across similar inputs.
* Achieved reliable grading of DME and detection of features without needing handcrafted logic.

---

##  **Future Scope:**

* Incorporate **transformer models** like BERT for better language understanding.
* Use **attention mechanisms** and external medical knowledge bases for enhanced reasoning.
* Extend the system to cover other diseases and imaging modalities (e.g., MRI, CT scans).


