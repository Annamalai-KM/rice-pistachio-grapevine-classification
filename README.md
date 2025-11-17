# Rice‑Pistachio‑Grapevine Classification

A Kaggle hackathon solution for leaf image classification of three crops: rice, pistachio, and grapevine. This repository contains an end-to-end Jupyter Notebook covering data preprocessing, model training (CNN / transfer learning), evaluation, and submission workflow. Finished Top 13 on the competition leaderboard.

---

## Short description

This project classifies leaf images into three classes:
- rice — images of rice leaves
- pistachio — images of pistachio leaves
- grapevine — images of grapevine leaves

The goal is to build a robust image classifier using transfer learning and practical augmentation, produce a validated model, and prepare a submission for the Kaggle competition.

---

## Key Features

- End-to-end notebook: preprocessing → modeling → evaluation → submission  
- Deep learning approach: convolutional neural network using transfer learning  
- Clear dataset structure and sample images for quick inspection  
- Visualizations and training diagnostics (loss / accuracy / confusion matrix)  
- Reproducible: requirements.txt, notebook seeds, and training settings included

---

## Sample Image Showcase

Below are embedded thumbnails pulled directly from this repository's Sample_Dataset.

Rice samples:
<p float="left">
  <img src="https://raw.githubusercontent.com/Annamalai-KM/rice-pistachio-grapevine-classification/main/Sample_Dataset/rice/0007.jpg" width="140" alt="rice 0007" />
  <img src="https://raw.githubusercontent.com/Annamalai-KM/rice-pistachio-grapevine-classification/main/Sample_Dataset/rice/0014.jpg" width="140" alt="rice 0014" />
  <img src="https://raw.githubusercontent.com/Annamalai-KM/rice-pistachio-grapevine-classification/main/Sample_Dataset/rice/0015.jpg" width="140" alt="rice 0015" />
</p>

Pistachio samples:
<p float="left">
  <img src="https://raw.githubusercontent.com/Annamalai-KM/rice-pistachio-grapevine-classification/main/Sample_Dataset/pistachio/0002.jpg" width="140" alt="pistachio 0002" />
  <img src="https://raw.githubusercontent.com/Annamalai-KM/rice-pistachio-grapevine-classification/main/Sample_Dataset/pistachio/0003.jpg" width="140" alt="pistachio 0003" />
  <img src="https://raw.githubusercontent.com/Annamalai-KM/rice-pistachio-grapevine-classification/main/Sample_Dataset/pistachio/0005.jpg" width="140" alt="pistachio 0005" />
</p>

Grapevine samples:
<p float="left">
  <img src="https://raw.githubusercontent.com/Annamalai-KM/rice-pistachio-grapevine-classification/main/Sample_Dataset/grapevine/0018.png" width="140" alt="grapevine 0018" />
  <img src="https://raw.githubusercontent.com/Annamalai-KM/rice-pistachio-grapevine-classification/main/Sample_Dataset/grapevine/0030.png" width="140" alt="grapevine 0030" />
  <img src="https://raw.githubusercontent.com/Annamalai-KM/rice-pistachio-grapevine-classification/main/Sample_Dataset/grapevine/0032.png" width="140" alt="grapevine 0032" />
</p>

Notes:
- Images above are confirmed to exist in Sample_Dataset/rice, Sample_Dataset/pistachio, and Sample_Dataset/grapevine. Filenames are case-sensitive.
- If you change the default branch from `main`, update the raw.githubusercontent.com URLs accordingly.


---

## Repository structure

A concise tree view of this repository (representative files shown):

```
.
├─ Sample_Dataset/
│  ├─ rice/
│  │  ├─ 0000.jpg
│  │  ├─ 0001.jpg
│  │  └─ 0002.jpg
│  │   ........
│  ├─ pistachio/
│  │  ├─ 0002.jpg
│  │  ├─ 0003.jpg
│  │  └─ 0005.jpg
│  │   .......
│  └─ grapevine/
│  │   ├─ 0018.png
│  │  ├─ 0030.png
│  │  └─ 0032.png
│  │   .......
├─ notebooks/
│  └─ notebook.ipynb           
├─ requirements.txt
├─ LICENSE
└─ README.md                        # end-to-end pipeline: preprocess → train → evaluate → submit
```

---

## How to run

1. Clone the repository:
```bash
git clone https://github.com/Annamalai-KM/rice-pistachio-grapevine-classification.git
cd rice-pistachio-grapevine-classification
```

2. Create a virtual environment and install dependencies:
```bash
python -m venv .venv
source .venv/bin/activate      # macOS / Linux
.venv\Scripts\activate         # Windows (PowerShell)
pip install --upgrade pip
pip install -r requirements.txt
```

3. Download the full dataset from Kaggle (dataset not included here):
```bash
# Requires Kaggle CLI and API token in ~/.kaggle/kaggle.json
kaggle competitions download -c <competition-name>
unzip <downloaded-zip> -d data/
```
Or, if it's a published dataset:
```bash
kaggle datasets download -d <owner>/<dataset-slug>
unzip <dataset-zip> -d data/
```

4. Open the notebook:
```bash
jupyter lab   # or jupyter notebook
# then open notebooks/notebook.ipynb and run cells sequentially
```

---

## Model & Evaluation Summary

- Approach: Transfer learning (pretrained CNN backbone) + custom head, augmentation, and class-balanced sampling.  
- Validation (holdout) results (example summary — see notebook for full logs):
  - Validation accuracy: ~93.2%
  - Macro F1-score: ~0.92  
- Final submission: ranked Top 13 on the public leaderboard.

See notebooks/notebook.ipynb for full training logs, checkpoint locations, and per-class metrics.

---

## Dataset information

- Source: Kaggle (competition / dataset page)  
- The full dataset is NOT included in this repository due to licensing and size constraints.  
- A small Sample_Dataset/ with representative images is included for development and README visualization.

---

## Technologies used

- PyTorch / Torchvision  
- Scikit-learn  
- Python 3.x, Jupyter Notebook  
- OpenCV, Pillow  
- NumPy, Pandas, Matplotlib / Seaborn

---

## License

This project is released under the MIT License. See LICENSE for details.

---
