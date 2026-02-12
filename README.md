**Buddiga Abhihske (AD23B1012)**  
B.Tech – Artificial Intelligence & Data Science  
Indian Institute of Information Technology, Raichur  


## Project 1: Brain Tumor Segmentation using Thresholding

## Dataset

- **Dataset Type:** Brain MRI Tumor Dataset  
- **Annotation Format:** YOLO Segmentation (Polygon-based)  
- **Data Split Used:** Training set  

### 📎 Kaggle Dataset Link  
https://www.kaggle.com/datasets/bilalakgz/brain-tumor-mri-dataset  

(Search for **Brain Tumor MRI YOLO Segmentation Dataset**)

---

## Methodology

### Ground Truth Generation
YOLO polygon annotations are converted into **binary tumor masks** using polygon filling. This allows pixel-wise comparison with predicted segmentations.

### Segmentation Techniques
- **Otsu Thresholding:** Uses a single global threshold to separate foreground and background.
- **Sauvola Thresholding:** Computes local adaptive thresholds based on neighborhood statistics.

### Evaluation Metrics
- **Dice Score**
- **Jaccard Index**

These metrics measure the overlap between predicted tumor regions and ground truth masks.

---

## Results

| Method | Dice Score | Jaccard Index |
|------|-----------|---------------|
| Otsu Thresholding | 0.1016 | 0.0579 |
| Sauvola Thresholding | 0.0650 | 0.0346 |

---

## Key Observations

- Otsu thresholding performed better when tumor intensity was clearly distinguishable.
- Sauvola thresholding was sensitive to noise and anatomical edges.
- Adaptive thresholding did not guarantee improved performance in MRI tumor segmentation.
- Classical thresholding methods have inherent limitations for medical images.
