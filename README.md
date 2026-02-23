# March Madness Kaggle 2026

This repository contains analysis, feature engineering, and modeling work for the Kaggle March Madness NCAA Tournament competition.

> Due to GitHub's file size limitations, raw competition datasets are not stored in this repository. You must download them directly from Kaggle.

---

## 1️⃣ Download the Data from Kaggle

1. Create a Kaggle account (if you do not already have one).
2. Navigate to the March Madness competition page on Kaggle.
3. Go to the **Data** tab.
4. Download the competition dataset ZIP file.
5. Extract the contents locally.

---

## 2️⃣ Project Folder Structure

Place the extracted CSV files into a folder named:

```
kaggle_data_sources
```

This folder should live in the root directory, alongside the notebook.

Example structure:

```
march_madness_kaggle_2026/
│
├── notebook.ipynb
├── kaggle_data_sources/
│   ├── MRegularSeasonDetailedResults.csv
│   ├── MNCAATourneyCompactResults.csv
│   ├── MMasseyOrdinals.csv
│   └── ...
│
├── .gitignore
└── README.md
```

> ⚠️ The `kaggle_data_sources/` directory is intentionally ignored by Git.

---

## 3️⃣ Optional: Download via Kaggle API (Recommended)

### Install Kaggle CLI

```bash
pip install kaggle
```

### Configure API credentials

1. Go to your Kaggle account settings.
2. Generate a new API token.
3. Place the downloaded `kaggle.json` file in:

```
~/.kaggle/
```

Then set permissions:

```bash
chmod 600 ~/.kaggle/kaggle.json
```

### Download the competition data

From the root of this repository:

```bash
kaggle competitions download -c <competition-name>
```

Unzip:

```bash
unzip <competition-name>.zip -d kaggle_data_sources
```

---

## 4️⃣ Why Data Is Not in the Repository

- GitHub enforces a 100MB file size limit.
- Some Kaggle datasets exceed this threshold.
- Versioning raw competition data is poor practice for ML workflows.
- The repository is designed to track code, experiments, and modeling logic — not static datasets.

---

## 5️⃣ Reproducibility Notes

All notebooks assume data exists at:

```
./kaggle_data_sources/
```

If you place the folder elsewhere, update the relative file paths accordingly.
