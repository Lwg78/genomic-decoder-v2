# Genomic Decoder (Fly) Version 2 (Improved)

A Transformer-based AI model (DNA-BERT) that predicts genomic features from *Drosophila melanogaster* (fruit fly) DNA sequences. This project demonstrates an end-to-end pipeline from raw biological data ingestion to neural network training.

## Project Structure

* **`01_Data_Prep.ipynb`**: The data engineering pipeline. It parses raw GTF annotation files, extracts DNA sequences from the genome (FASTA), and matches them with labels from a Single-Cell Atlas.
* **`02_Model_Architecture.ipynb`**: The blueprint. It defines the custom DNA Tokenizer and the Encoder-only Transformer architecture (DNA-BERT).
* **`03_Model_Training.ipynb`**: The training engine. It implements the training loop, loss calculation, and visualization of the learning curve.

## How to Run

1.  **Install Dependencies:**
    Ensure you have the required libraries installed.
    ```bash
    pip install -r requirements.txt
    ```

2.  **Prepare Data:**
    Run `01_Data_Prep.ipynb` first. This will check for the raw data files in `data/raw/` and generate the `training_manifest.csv` needed for the model.

3.  **Train Model:**
    Run `03_Model_Training.ipynb`. This will load the manifest, initialize the Transformer, and train it to predict genomic features (e.g., GC content).

## Requirements
* Python 3.11+
* PyTorch
* Scanpy
* Biopython
