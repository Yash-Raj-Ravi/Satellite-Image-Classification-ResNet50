# Satellite Image Classification using ResNet50

## Project Overview
This project classifies satellite images from the EuroSAT dataset using a deep learning model based on ResNet50 and transfer learning.

The model was trained in two phases:
1. Feature extraction with all ResNet50 layers frozen.
2. Fine-tuning by unfreezing the last 30 layers of ResNet50.

## Dataset
- Dataset: EuroSAT
- Classes: 10 land-use and land-cover categories
- Image Type: RGB satellite images

## Model Architecture
- Base Model: ResNet50 (pre-trained on ImageNet)
- Transfer Learning
- Global Average Pooling
- Dense Classification Layer
- Softmax Activation

## Training Strategy

### Phase 1: Feature Extraction
- All ResNet50 layers frozen
- Validation Accuracy: **95.37%**

### Phase 2: Fine-Tuning
- Unfroze last 30 layers
- Reduced learning rate
- Validation Accuracy: **98.02%**
  
### Training Enhancements
- Data augmentation for improved generalization
- Transfer learning using ImageNet pretrained weights
- Fine-tuning of the final 30 ResNet50 layers

## Results

| Training Phase | Validation Accuracy |
|---------------|--------------------|
| Frozen ResNet50 | 95.37% |
| Fine-Tuned ResNet50 | 98.02% |

## Technologies Used
- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Scikit-Learn
- Google Colab

## Repository Contents

- `Resnet CNN_Model.ipynb` – Model training and fine-tuning
- `Accuracy_Plots.ipynb` – Training visualization and evaluation

## Future Improvements
- Compare performance with EfficientNet and Vision Transformers (ViT)
- Perform hyperparameter optimization using Optuna/Grid Search
- Deploy the model as a web application using Streamlit or Flask
- Extend the model to higher-resolution satellite imagery datasets
- Experiment with ensemble learning techniques

## Author
Yash Raj Ravi
