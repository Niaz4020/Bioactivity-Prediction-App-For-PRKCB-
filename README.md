# Bioactivity Prediction App (PRKCB)

This repository contains a **bioactivity prediction web app** built with **Python** and **Streamlit**.  
The app predicts the inhibitory activity (pIC50) of molecules against **PRKCB (Protein kinase C beta type)** — a drug target for **Diabetic Nephropathy**.

----

## 🚀 Features
- Upload molecules in `.txt` format (SMILES).
- Automatic molecular descriptor calculation using **PaDEL-Descriptor**.
- Predict bioactivity (pIC50) using a pre-trained **machine learning model**.
- Download prediction results as `.csv`.
- Interactive visualization in the browser.

---

## 📂 Project Structure
```
├── app.py                           # Streamlit app source code
├── bioactivity_prediction_app_PRKCB.ipynb  # Jupyter notebook for model building
├── PRKCB_model.pkl                  # Pre-trained ML model
├── descriptor_list.csv              # Descriptor subset used in model
├── PaDEL-Descriptor/                # PaDEL-Descriptor JAR + config files
├── logo.png                         # App logo
```

---

## 🛠️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/your-username/bioactivity-prediction-prkcb.git
cd bioactivity-prediction-prkcb
```

### 2. Create and activate environment
```bash
conda create -n bioenv python=3.9 -y
conda activate bioenv
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

### 1. Run the Streamlit app
```bash
streamlit run app.py
```

### 2. Upload input molecules
- Prepare a `.txt` file with **SMILES** strings and molecule names (space-separated).
- Upload the file via the sidebar in the app.

### 3. Get predictions
- Descriptors will be calculated automatically using **PaDEL-Descriptor**.
- Model predictions (`pIC50`) will be displayed in the app.
- Results can be downloaded as a CSV.

---

## 📊 Example Input Format
Example `molecule.smi`:
```
CCOc1ccc2nc(S(N)(=O)=O)sc2c1 Molecule1
CCN(CC)CCCC(C)Nc1ccc(OC)cc1 Molecule2
```

---

## 📖 References
- **PaDEL-Descriptor:** [Software](http://www.yapcwsoft.com/dd/padeldescriptor/) | [Paper](https://doi.org/10.1002/jcc.21707)  
- **Dataprofessor’s Cheminformatics tutorials**  

---

## 👨‍💻 Credits
- Developed by **S M Riaduzzaman Niaz**  
- Based on open-source cheminformatics workflows  
- Credit to [Chanin Nantasenamat](https://medium.com/@chanin.nantasenamat) (aka [Data Professor](http://youtube.com/dataprofessor)) 
