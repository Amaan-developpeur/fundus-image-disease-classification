# Fundus Image Disease Classification

This repository contains a Jupyter Notebook that implements a deep learning pipeline to classify retinal fundus images into four categories: Cataract, Diabetic Retinopathy, Glaucoma, and Normal.

## Repository Structure

```
fundus-disease-classification/
├── notebook.ipynb         # Main Jupyter Notebook
├── requirements.txt       # Python dependencies
├── .gitignore             # Files to ignore in Git
└── split/                 # Dataset folder (download manually)
    ├── train/             # Training images
    ├── val/               # Validation images
    └── test/              # Test images
```

## Dataset

1. Download the dataset from:

   > [https://www.kaggle.com/datasets/drskprabhakar/cataract-dr-normal-glaucoma-fundus-images-dataset](https://www.kaggle.com/datasets/drskprabhakar/cataract-dr-normal-glaucoma-fundus-images-dataset)
2. Unzip or extract so that the top-level folder is named `split`, containing `train/`, `val/`, and `test/` subfolders.
3. Place the entire `split/` folder at the root of this repository, alongside `notebook.ipynb`.




## Setup

1. **Clone this repository**

   ```bash
   git clone https://github.com/Amaan-developpeur/fundus-disease-classification.git

   cd fundus-disease-classification
   ```

2. **Create a virtual environment (optional but recommended)**

   ```bash
   python -m venv venv
   source venv/bin/activate       # macOS/Linux
   venv\Scripts\activate        # Windows
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Verify dataset placement**
   Ensure the `split/` folder (with `train/`, `val/`, `test/`) lives here:

   ```bash
   ls
   # you should see:
   # notebook.ipynb  requirements.txt  split/
   ```

## Running the Notebook

* Launch Jupyter Lab or Notebook:

  ```bash
  jupyter notebook
  ```
* Open `notebook.ipynb` and run cells from top to bottom.

## Notebook Outline

1. **Step 1: Data Setup** — Verify folder structure and list classes.
2. **Step 2: Data Inspection** — Image counts, sample viewing, blur & quality checks.
3. **Step 3: Data Generators** — Define `ImageDataGenerator` for train/val/test.
4. **Step 4: Baseline CNN** — Build & train a custom CNN from scratch.
5. **Step 5: Transfer Learning** — Feature extraction and fine-tuning with MobileNetV2.
6. **Step 6: Logistic Regression Head** — Frozen backbone + logistic classifier.
7. **Step 7: Evaluation & Interpretation** — Confusion matrices, classification reports, Grad-CAM.
8. **Step 8: Conclusion & Future Work**

## Requirements

Contents of `requirements.txt`:

```
tensorflow>=2.10
keras
numpy
pandas
matplotlib
scikit-learn
opencv-python
Pillow
```

(Adjust versions as needed.)

## Disclaimer

*This notebook and the resulting model are for academic and research purposes only.This is a prototype model to assist the domain experts but  ********not******** diagnostic tool.*

---
