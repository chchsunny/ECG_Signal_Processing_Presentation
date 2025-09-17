# ECG_Signal_Processing_Presentation
This project applies machine learning to ECG signal processing using the MIT-BIH databases. We implemented preprocessing, feature extraction, and classification using SVM, Random Forest, and KNN.
## 📊 Dataset

The project uses the following **PhysioNet MIT-BIH Databases**:

- [MIT-BIH Arrhythmia Database](https://physionet.org/content/mitdb/1.0.0/)
- [MIT-BIH Supraventricular Arrhythmia Database (SVDB)](https://physionet.org/content/svdb/1.0.0/)
- [MIT-BIH Normal Sinus Rhythm Database (NSRDB)](https://physionet.org/content/nsrdb/1.0.0/)

⚠️ **Note**: Due to licensing, the raw datasets are **not included** in this repository.  
Please download them manually from [PhysioNet](https://physionet.org).

---

## ⚙️ Methods

1. **Signal Preprocessing**
   - Filtering  
   - R-peak detection  

2. **Feature Extraction**
   - **PQRST features**:  
     - P-wave amplitude  
     - QRS amplitude  
     - T-wave amplitude  
     - QRS duration  
   - **HRV features**:  
     - Mean RR Interval  
     - SDNN  
     - RMSSD  
     - NN50  
     - pNN50  

3. **Sample Preparation**
   - Resample (128Hz → 360Hz)  
   - Segment ECG into **30s windows**  
   - Label samples as **normal (0)** or **abnormal (1)**  
   - Train/Test split (80%/20%)  
   - Balance dataset  

4. **Model Training**
   - SVM  
   - Random Forest (optimized with GridSearchCV)  
   - KNN  

---

## start up

點擊下方按鈕，即可在 Google Colab 中直接執行

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/ECG-Signal-Processing-ML/blob/main/notebooks/ECG_Feature_Extraction.ipynb)

---

## Results

- Random Forest performed best with ~97.9% accuracy.  
- Most important features:  
  - P-wave amplitude (0.1995)  
  - QRS amplitude (0.1826)  
  - Mean RR Interval (0.1517)  
  - QRS duration (0.1309)  

Confusion matrices and feature importance plots are available in the `results/` folder.

---

## License
This project is licensed under the MIT License – see the LICENSE
 file for details.
