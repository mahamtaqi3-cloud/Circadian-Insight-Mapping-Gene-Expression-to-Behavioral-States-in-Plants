# Circadian Insight: Mapping Gene Expression to Behavioral States in Plants

---

### 🧬 Project Overview

This project leverages machine learning to decode the **Circadian Clock** of *Arabidopsis thaliana*. By analyzing high-dimensional genomic expression data, we demonstrate that a plant’s temporal state—its "internal time"—can be accurately predicted from its transcriptome.

We successfully transitioned from massive, noisy genomic datasets to identifying **high-confidence circadian biomarkers**, bridging the gap between raw data and core biological regulatory networks.

---

### 🚀 Key Technical Achievements

* **Data Pipeline:** Developed a robust workflow to ingest and transform complex GEO datasets into a clean, machine-learning-ready matrix.
* **Dimensionality Reduction:** Implemented variance-based feature selection to overcome the "Curse of Dimensionality," effectively filtering >50,000 probes down to the most biologically relevant markers.
* **Predictive Modeling:** Trained a `RandomForestClassifier` to discretize and predict circadian phases (Morning, Day, Evening, Night) with high accuracy.
* **Rigorous Validation:** Employed `Leave-One-Out` cross-validation to ensure the model learns biological signatures rather than memorizing individual samples.

---

### 🧠 Understanding the Biology

The model identifies the **"molecular clock"** of the plant. The top-performing features are not just random probes—they are master regulators that dictate plant behavior.

By mapping our model's top feature identifiers (`ID_REF`) to official gene symbols via the **TAIR database**, we confirmed that the model autonomously highlights key clock-regulated genes, such as:

* ***CCA1*** (Circadian Clock Associated 1)
* ***TOC1*** (Timing of CAB expression 1)
* ***LHY*** (LATE ELONGATED HYPOCOTYL)

---

### 📊 Project Architecture

The pipeline follows a proven systems biology workflow:

| Stage | Action | Purpose |
| --- | --- | --- |
| **Ingestion** | `GEOParse` | Import raw genomic profiles. |
| **Engineering** | Variance Filtering | Remove noise and focus on oscillating genes. |
| **Modeling** | `RandomForestClassifier` | Predict phase from gene expression. |
| **Validation** | `LeaveOneOut` | Ensure honest, non-overfitted results. |
| **Discovery** | ID Mapping | Translate probes to biological gene symbols. |

---

### 💡 Why This Matters

This project confirms that **gene expression profiles act as a fingerprint for temporal behavior.** By understanding these genomic signatures, we provide a blueprint for how complex biological behaviors—such as the circadian rhythm—can be inferred, mapped, and predicted through machine learning.

---

### 🛠️ Built With

* **Python:** The core engine for data processing.
* **Scikit-Learn:** Used for robust machine learning and model evaluation.
* **Pandas/Numpy:** Essential for high-speed matrix manipulation.
* **Matplotlib:** For visualizing gene importance and model performance.

---

*Developed as a capstone exploration into genomic variant prediction and behavioral phenotyping.*

