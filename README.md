# ECG_Signal_Processing_Presentation
Machine learning applied to ECG signal processing using MIT-BIH dataset
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
