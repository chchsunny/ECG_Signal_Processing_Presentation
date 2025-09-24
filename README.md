# Machine learning applied to ECG signal analysis
本專案利用MIT-BIH資料庫，將機器學習應用於心電圖訊號處理，使用SVM、Random Forest和KNN，比較三種方法的預測能力。

---

## Dataset

本專案使用以下 **MIT-BIH 資料庫**：

- [MIT-BIH Arrhythmia Database](https://physionet.org/content/mitdb/1.0.0/)
- [MIT-BIH Supraventricular Arrhythmia Database (SVDB)](https://physionet.org/content/svdb/1.0.0/)
- [MIT-BIH Normal Sinus Rhythm Database (NSRDB)](https://physionet.org/content/nsrdb/1.0.0/)

---

##  Methods

1. **訊號前處理**
   - Filtering
   - R-peak detection

2. **特徵擷取**
   - **PQRST 特徵**:  
     - P-wave amplitude  
     - QRS amplitude  
     - T-wave amplitude  
     - QRS duration  
   - **HRV 特徵**:  
     - Mean RR Interval  
     - SDNN  
     - RMSSD  
     - NN50  
     - pNN50  

3. **樣本準備**
   - 重新取樣 (128Hz → 360Hz)  
   - 將 ECG 分割為 30 秒片段 
   - Label samples 標註為 normal (0) or abnormal (1) 
   - Train/Test 分割 (80%/20%)  
   - 平衡樣本

4. **模型訓練**
   - SVM  
   - Random Forest (optimized with GridSearchCV)  
   - KNN  

---

## start up

---

## Results
<img width="683" height="280" alt="image" src="https://github.com/user-attachments/assets/bce96c09-beb1-4578-8a9c-350714f7f0fe" />

<img width="678" height="404" alt="image" src="https://github.com/user-attachments/assets/0f61fe76-c9b8-4862-8c7c-db2f5c6163b7" />

---

## License
本專案使用 MIT License 授權，歡迎自由使用與參考
