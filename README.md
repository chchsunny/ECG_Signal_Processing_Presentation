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
<img width="683" height="280" alt="image" src="https://github.com/user-attachments/assets/bce96c09-beb1-4578-8a9c-350714f7f0fe" />

<img width="678" height="404" alt="image" src="https://github.com/user-attachments/assets/0f61fe76-c9b8-4862-8c7c-db2f5c6163b7" />

 Confusion matrices and feature importance plots are available in the `results/` folder.

---

## License
This project is licensed under the MIT License – see the LICENSE
 file for details.
