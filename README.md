# SVM-based-seizure-detection
## Dataset
CHB-MIT Scalp EEG Database https://physionet.org/content/chbmit/1.0.0/
## Method
### Preprocessing 
EEG data is subject to many artifacts such as line noise, electrical noise and movement artifact. For the purpose of this project, patient label chb24's data of 6 electrode channels: F3C3, C3P3, F4C4, C4P4, CZPZ and P7T7 were chosen due to it's frequent occurrence of seizures and signal clarity.
### Feature Extraction
Power in the following 7 different spectral bands from each of the 6 electrode channels was extracted in half-overlapping windows of 20 seconds: delta (0.5-4Hz), theta (4-8Hz), alpha (8-13Hz), beta (13-30Hz), gamma1 (30-57Hz), gamma2 (63-128Hz) and total power.
### Classification
An 11-fold cross validation was implemented using a support vector machine and the gamma parameter is optimized based on the percentage of correct classification of an onset seizure.
### Results
Best model accuracy is 0.69 beating chance accuracy which is around 0.55.
### Further Improvements
To include ROC curves and prediction discrepancy rate…
To include more features, consider all channels or choose best channels for each patient…
