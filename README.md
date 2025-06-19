# GenerativeAI-NCD-Monitoring

This project presents a deep learning–based healthcare system that uses Generative Adversarial Networks (GANs), transformer models, and diffusion-based imputation to support the monitoring and prediction of non-communicable diseases (NCDs) such as diabetes, cardiovascular conditions, and hypertension. It focuses on improving diagnostic support in clinical settings, especially where incomplete, imbalanced, or low-volume data is common.

The solution integrates AI with healthcare data systems to generate synthetic samples, predict risk progression from patient histories, and handle missing values—all while ensuring clinical transparency using explainable AI (XAI) tools like SHAP and LIME.

## Features

- Transformer-based modeling for NCD risk prediction
- GANs for generating synthetic patient data
- Diffusion models to impute missing health records
- Modular architecture: data prep, modeling, explainability
- Compatible with structured datasets (CSV, JSON, FHIR-ready)

## Tech Stack

| Component                 | Tool/Library                      |
|--------------------------|-----------------------------------|
| Data Generation          | GANs (PyTorch)                    |
| Prediction Models        | Transformers (HuggingFace)        |
| Imputation               | Diffusion models (custom)         |
| Explainability           | SHAP, LIME                        |
| Data Handling            | NumPy, Pandas, Scikit-learn       |
| Language                 | Python 3.8+                       |

## Architecture Structure

```
          +---------------------------+
          |  Patient Historical Data  |
          +---------------------------+
                        |
                        v
     +------------------+------------------+
     | Preprocessing & Normalization       |
     +------------------+------------------+
                        |
                        v
     +------------------+------------------+
     |  Generative Model (GANs)            |
     |  - Generate synthetic records       |
     +------------------+------------------+
                        |
                        v
     +------------------+------------------+
     |  Prediction Model (Transformer)     |
     |  - Time-series risk scoring         |
     +------------------+------------------+
                        |
                        v
     +------------------+------------------+
     |  Imputation Model (Diffusion)       |
     |  - Fill missing entries             |
     +------------------+------------------+
                        |
                        v
     +------------------+------------------+
     | Explainability & Reporting (SHAP)   |
     +-------------------------------------+
```

## Installation & Setup

### System Requirements

- Python 3.8+
- pip installed
- Virtual environment recommended

### Setup Instructions

```bash
git clone https://github.com/yourusername/GenerativeAI-NCD-Monitoring.git
cd GenerativeAI-NCD-Monitoring
pip install -r requirements.txt
```

To run the system:

```bash
python main.py
```

## Motivation

In real-world clinical environments, health datasets are often incomplete, noisy, or limited in scale. Traditional models fail when missing entries or small sample sizes impact prediction accuracy. This system was motivated by the need to:

- Use generative AI to balance underrepresented classes (e.g., rare conditions)
- Fill in missing patient records without manual interpolation
- Make clinical predictions explainable and trustworthy

## Difficulties Faced

- Lack of large, clean, open-source NCD datasets for training
- Handling instability during GAN training
- Fine-tuning transformers for healthcare-specific vocabulary
- Interpreting imputed values and explaining model outputs to non-technical users

## Project Timeline

| Phase                             | Duration     | Key Tasks                                                                 |
|-----------------------------------|--------------|---------------------------------------------------------------------------|
| Phase 1: Research & Design        | Weeks 1–3    | Literature review, define use cases, choose model architectures           |
| Phase 2: Core Implementation      | Weeks 4–7    | Implement GANs, transformers, and diffusion modules                       |
| Phase 3: XAI & Evaluation         | Weeks 8–10   | Add SHAP/LIME explainability, tune models, generate evaluation metrics    |
| Phase 4: Integration & Reporting  | Weeks 11–14  | Integrate modules, write documentation, finalize codebase and upload      |

## Expected Outcomes

| Category                      | Expected Outcome                                                                                       |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| NCD Risk Prediction          | Use of transformer models to predict chronic disease progression with higher accuracy                  |
| Synthetic Data Generation    | GANs will generate statistically similar but artificial patient records for class balancing            |
| Missing Data Imputation      | Diffusion models fill missing lab values and vitals with minimal noise and high precision              |
| Explainability               | Use SHAP/LIME to provide transparent model decisions to clinicians and researchers                     |
| Clinical Utility             | Provide scalable, modular AI solutions that can plug into hospitals or EHR systems                    |
| Ethical Compliance           | Ensure anonymization, privacy-preserving design, and interpretable outputs                             |

## License

This project is licensed under the MIT License.

## Contact

- Name: Sampada Vikrant Kabule
- LinkedIn: [linkedin.com/in/sampada-kabule-4728642b3](https://www.linkedin.com/in/sampada-kabule-4728642b3)
- Email: sampadakabule03@gmail.com
