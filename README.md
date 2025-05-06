# 🚗 Car Damage Detection using Deep Learning

This project is focused on detecting **car damage types** from images using deep learning. The model classifies a car image into one of the following **6 categories**:

- **Front Normal**
- **Front Crushed**
- **Front Breakage**
- **Rear Normal**
- **Rear Crushed**
- **Rear Breakage**

## 📁 Dataset

- Total Images: ~1700
- Classes: 6 (as mentioned above)
- Input: Car images
- Preprocessing: Data augmentation techniques (rotation, zoom, flip, etc.) to enhance model generalization.

## 🧠 Approach

### 1. 📊 Baseline Model (CNN)
- **Technique**: Custom CNN
- **Accuracy**: 57%
- **Observation**: Underfitting, struggled to generalize.

### 2. 🔒 CNN with Regularization
- **Techniques**: Added Dropout & L2 Regularization
- **Accuracy**: 55%
- **Observation**: Regularization didn’t help, accuracy dropped.

### 3. 🔁 Transfer Learning - EfficientNet
- **Model**: EfficientNet
- **Accuracy**: 69%
- **Observation**: Performance improved significantly with pre-trained weights.

### 4. 🌀 ResNet with Dropout
- **Model**: ResNet (with Dropout = 0.5, Learning Rate = 0.001)
- **Accuracy**: 84%
- **Observation**: Best result so far, good balance between bias and variance.

### 5. 🔍 Hyperparameter Tuning with Optuna
- **Search Space**:
  - Learning Rate: `[1e-5, 1e-2]`
  - Dropout: `[0.2, 0.7]`
- **Best Found**: 
  - Learning Rate: `0.001`
  - Dropout: `0.28`
- **Accuracy**: 83%
- **Observation**: Despite optimized parameters, performance slightly dropped. Reverted to Dropout = 0.5.

## 🧪 Final Model

| Model     | Accuracy |
|-----------|----------|
| CNN       | 57%      |
| CNN + Reg | 55%      |
| EfficientNet | 69%   |
| ResNet (LR=0.001, Dropout=0.5) | **84%** |
| Optuna Tuned | 83%   |

## 🛠️ Tools & Libraries Used

- Python
- PyTorch
- PIL
- Matplotlib
- Optuna for hyperparameter tuning
- Jupyter Notebook

## 📌 Future Improvements

- Train on larger and more diverse dataset
- Test with real-world car images
- Deploy the model using Flask or Streamlit
- Implement Grad-CAM for damage localization

## 📷 Sample Predictions

## 📷 Sample Predictions

![Car Damage Detection GIF](https://github.com/Rohesen/car-damage-detection-app/blob/main/project_video.gif)



