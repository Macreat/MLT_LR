# MLT_LR

## Learning route of my Machine Learning Theory course at UNAL 2025

_Learning path in Machine Learning Theory and Practical Development (UNAL 2025)_

![status](https://img.shields.io/badge/status-active-brightgreen)
![made-with](https://img.shields.io/badge/Made%20with-ScikitLearn-orange)
![platform](https://img.shields.io/badge/platform-VSCode-lightgrey)
![python](https://img.shields.io/badge/python-3.10%2B-blue)

---

## Description

This repository documents my **learning route in Machine Learning Theory (MLT)**,  
including:

- **Notebooks and experiments** for practical model implementation.
- **Optimization workflows** (Bayesian, Optuna, skopt).
- **Theoretical material**: books, notes, and references.
- **Development environment** to run and reproduce results.
- **Cloned repositories** for study, testing, and integration.

---

## Branch Strategy

To keep the work organized, this repo uses a **branching model**:

- **`main`**  
  Main branch. Contains **stable, reviewed, and clean code/documentation**.  
  Always reflects the state of the project that is ready to be delivered or referenced.

- **`dev`**  
  Development branch. Contains **ongoing work** and integrates features before merging into `main`.  
  All new features or experiments should be branched off `dev`.

---

## Repository Structure

MLT_LR/  
├── .gitignore # Git ignored files (at repo root)  
├── README.md # Main repository description (at repo root)  
│  
└── mltEnv/ # Python virtual environment + main repo structure  
│ ├── Include/ # venv internal  
│ ├── Lib/ # venv internal  
│ ├── Scripts/ # venv internal  
│ ├── README.md # Readme to describe development environment  
│  
│ ├── cloneRepo/ # Cloned repositories from professors or external projects  
│ │ └── README.md  
│  
│ ├── content/ # Study materials and resources on ML theory  
│ │ ├── books/ # Books and references  
│ │ └── README.md  
│
│  
│ ├── work/ # Includes organized submissions, project ,reports, and deliverables  
│ │ └── README.md  
│
│  
└── requirements.txt # Dependencies for reproducibility (on a future after some model implementation )

## how to RUN nbs

### 1. Set up the environment (example with Python venv)

```bash
# Create virtual environment
python -m venv mltEnv

# Activate it
source mltEnv/bin/activate     # Linux/Mac
.\mltEnv\Scripts\activate      # Windows PowerShell

# Install dependencies
pip install -r requirements.txt
```

Then ,navigate to the correct folder depending on task:
-DevContent/ → Run and develop Jupyter notebooks or ML scripts.
-content/ → Access theory, books, and lecture notes.
-work/ → View reports, deliverables, and documentation.
-cloneRepo/ → external repositories.

In order to run notebooks,

```bash
From the repo root : jupyter notebook work/
```

or open the .ipynb files directly in VSCode with the Python extension, also you can download and import on colab or any other environment.

---

## Projects and Experiments

- **Algebra and probabilistic analysis** as a foundation for deeper comprehension of model architectures.
- **Gradient Descent and regressors** approaches for linear models.
- **Bayesian Optimization** for kernel ridge regression.
- **Housing datasets** (California, etc.) with analytical + iterative methods.
- **NFL Big data bowl 2026** to predict player movement while the ball is in the air.

---

## Notes and Resources to develop

All inside PYDevEnv/:

- **Books & class PDFs** → [content/ss'sBooks/](./PYDevEnv/content/)
- **Class notes & theory** → [content/lectures/](./PYDevEnv/content/lectures/)
- **work class** → [work/](./PYDevEnv/work/)

---

## Roadmap

- [x] Create README base
- [x] Add repo structure
- [x] Upload repo from course
- [x] Document first experiments and tasks (linear regression, Bayesian optimization)
- [x] First partial test (ML on NFL DB)
- [x] Deliver work as:
  - assigned tasks
  - mathematical/model demonstrations
- [x] second test (DL on NFL DB)
- [ ] Project

## Author

**Mateo Almeida (Macreat)**

Course: Machine Learning Theory @ UNAL 2025

GitHub: [@Macreat](https://github.com/Macreat)

## License

License: **no**

Usage: Academic and learning purposes
