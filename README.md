# Visual Search Engine with EfficientNetV2 & PCA

This project implements an **Image Retrieval System** (Reverse Image Search) using deep learning. It allows users to search for visually similar images within a dataset by comparing their high-dimensional feature representations rather than simple pixel values.

---

##  Key Features
* ** Feature Extraction:** Utilizes the state-of-the-art **EfficientNetV2-S** model (pretrained on ImageNet) to capture complex visual patterns.
* **Efficiency with PCA:** Employs **Principal Component Analysis (PCA)** to compress 1280-dimensional feature vectors into a compact form, significantly accelerating the search process while maintaining accuracy.
* **Semantic Similarity:** Uses **Cosine Similarity** to rank and retrieve the top-most relevant images based on the query input.
* **Dataset Support:** Native support for the **Caltech 101** dataset, which includes 101 diverse object categories.

---

##  Tech Stack
* **Deep Learning Framework:** PyTorch
* **Computer Vision:** Torchvision (EfficientNetV2-S)
* **Machine Learning Tools:** Scikit-learn (PCA)
* **Data Processing:** NumPy, PIL (Pillow)
* **Visualization:** Matplotlib

---

##  How to Use

Follow these steps to set up and run the visual search engine:

### 1. Prerequisites
Install the required Python libraries:
```bash
pip install torch torchvision scikit-learn matplotlib tqdm pillow
```

### 2. Dataset Setup
The project is configured to work with the **Caltech 101** dataset.
* The notebook includes scripts to load/download the dataset automatically.
* Images are pre-processed (resized and normalized) to meet the requirements of the **EfficientNetV2-S** model.

### 3. Execution Pipeline
1.  **Initialize Model:** Load the pretrained `efficientnet_v2_s` weights and set it to evaluation mode.
2.  **Feature Extraction:** Run the extraction loop to generate "embeddings" for every image in your dataset.
3.  **Apply PCA:** Fit the PCA model on the extracted features to reduce dimensionality and noise.
4.  **Search/Query:** Provide a query image to the search function to visualize the **Top-5** most similar results from the database.

---


### Author

- **Salem Zain Alaidaroos**
- Computer Science Student
- AI and Software Engineering Enthusiast
