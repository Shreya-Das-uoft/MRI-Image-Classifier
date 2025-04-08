# 🧠 MRI Brain Tumor Classifier

Welcome to the **MRI Image Analyzer** project! This notebook guides you through building a Convolutional Neural Network (CNN) to classify MRI brain scans into **Tumor** and **Normal** categories using TensorFlow and OpenCV. The dataset used contains real MRI scans from Kaggle.

---

## 📂 Dataset

The dataset comes from Kaggle:  
📎 [MRI-based Brain Tumor Images](https://www.kaggle.com/datasets/mhantor/mri-based-brain-tumor-images)

It includes colored `.jpg` images categorized into:
- Tumor 🧠
- Normal 🧠

The data is split into:
- Training
- Validation
- Testing

---

## 🛠️ Project Setup

Create and activate a virtual environment:

```bash
python -m venv env
source env/bin/activate
```

Install the required dependencies:

```bash
pip install tensorflow opencv-python matplotlib
```

---

## 🧹 Preprocessing

Although the images are all `.jpg` and Python-compatible, the project includes a basic OpenCV test to confirm the integrity of image loading. Color channels are converted from BGR to RGB using:

```python
cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
```

---

## 🧪 Model Building

Using TensorFlow/Keras, we build a CNN architecture tailored to medical image classification tasks. This includes:

- Image resizing & normalization
- Data augmentation
- CNN model with convolution, pooling, and dense layers
- Model compilation & training
- Evaluation on test data

---

## 🧠 Why It Matters

Detecting brain tumors early is crucial. Deep learning models, especially CNNs, have shown high accuracy in medical imaging tasks ([Esteva et al., 2017](https://www.nature.com/articles/nature21056)). With clean preprocessing and properly split datasets, this project aims to demonstrate such potential.

---

## 🧾 Citation & Acknowledgements

- **Dataset**: MRI-based Brain Tumor Images from [Kaggle](https://www.kaggle.com/datasets/mhantor/mri-based-brain-tumor-images)
- **Original Notebook**: [GitHub Repo](https://github.com/Shreya-Das-uoft/MRI-Image-Classifier) by *Shreya Das*
- **Test Images**:
Prakash, B.V., Kannan, A.R., Santhiyakumari, N. et al. Meningioma brain tumor detection and classification using hybrid CNN method and RIDGELET transform. Sci Rep 13, 14522 (2023). https://doi.org/10.1038/s41598-023-41576-6.

Kayalı, Devrim & Çevik, U.. (2018). Detection And 3D Modeling Of Brain Tumors Using Image Segmentation Methods And Volume Rendering. International Journal of Natural and Engineering Sciences. 3. 79-86.

Gaikwad, Sonali & Joshi, M.. (2015). Brain Tumor Classification using Principal Component Analysis and Probabilistic Neural Network. International Journal of Computer Applications. 120. 5-9. 10.5120/21205-3885.

---

## 🚀 Future Work

- Build an app, where people can upload there own MRI images for classification
- Although the model had high accuracy with the testing data from the dataset, it had trouble classifying MRI images with an eyeball present. Next step would be to train the model on these images too.
