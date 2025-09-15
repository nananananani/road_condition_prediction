# Road Condition Prediction  ⋆.
. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁. ݁₊ ⊹ . ݁˖ . ݁

This project is a beginner's version of a Computer Vision model that detects potholes on roads from images.
It used a pretrained MobileNetV2 model to classify images as either **Normal** or **Pothole**.

## Dataset
* The dataset used is taken from Kaggle: [Pothole Detection Dataset](https://www.kaggle.com/datasets/atulyakumar98/pothole-detection-dataset)
* The dataset contains two clauses:
   * 'Normal' -> Roads without potholes
   * 'Pothole' -> Roads with potholes
## Preprocessing

1. Resize all images to **224x224 pixels**.
2. Convert images to **PyTorch tensors**.
3. Load dataset using `torchvision.datasets.ImageFolder`.
4. Use `DataLoader` to create **batches** and shuffle data.

## Workflow 

1. **Model Selection**  
   - Used **MobileNetV2** with **pretrained ImageNet weights** for faster convergence.
   - Replaced final layer to output **2 classes** (Normal / Pothole).

2. **Training**  
   - Loss function: `CrossEntropyLoss`  
   - Optimizer: `Adam`  
   - Epochs: 3 (for demo purposes)  
   - Device: GPU if available, otherwise CPU.

3. **Evaluation**  
   - Calculate **accuracy** per epoch.
   - Track **loss** to monitor learning.

4. **Visualization**  
   - Display sample images with model predictions.
   - Save trained model for future inference.

## Results 
- Training Accuracy: **~96-97%**
- Loss: Low, showing good convergence.

  <img width="539" height="125" alt="image" src="https://github.com/user-attachments/assets/be25e1f8-c60c-4c80-9155-01e201da0788" />

  <img width="661" height="678" alt="image" src="https://github.com/user-attachments/assets/c0f46477-746d-4dcb-809e-f8c295036e9a" />

| Image | Prediction |
|-------|-----------|
| 1 | Normal |
| 2 | Pothole |
| 3 | Normal |
| 4 | Pothole |


  
