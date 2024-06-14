
# Cat and Dog Classifier

This project demonstrates a machine learning model that classifies images of cats and dogs using Convolutional Neural Networks (CNN). The model was built and trained using Python and various machine learning libraries.

## Introduction
This project aims to classify images of cats and dogs using CNNs. We trained multiple models and compared their performance to determine the most accurate one.

## Dataset
The dataset consists of 37,461 images of cats and dogs divided into three subsets:
- Training: 20,000 images (10,000 cats and 10,000 dogs)
- Testing: 12,461 images (6,219 cats and 6,242 dogs)
- Validation: 5,000 images (2,500 cats and 2,500 dogs)

The images are in JPG format and vary in resolution.

## Preprocessing
- Inconsistent images were manually removed.
- All images were resized to 224x224 pixels.
- The dataset was split into training and testing subsets with an 80-20 split.

## Model Architecture
We experimented with several pre-trained CNN architectures:
- **Model A1**: ResNet-50 with 14 frozen layers
- **Model A2**: ResNet-50 with 88 frozen layers
- **Model A3**: ResNet-50 with 174 frozen layers
- **Model B**: MobileNetV3-Small

## Training
- Batch size: 32
- Epochs: 15
- Learning rate: 0.00012 (determined using ktrain's `lr.find()` function)
- Data augmentation: Random horizontal flipping

## Results
| Model  | Accuracy  | Loss   | Training Time |
|--------|-----------|--------|---------------|
| A1     | 99.21%    | 2.90%  | 60 min        |
| A2     | 99.34%    | 2.81%  | 34 min        |
| A3     | 98.47%    | 18.23% | 22 min        |
| B      | 97.14%    | 11.54% | 21 min        |

The results indicate that Model A2 (ResNet-50 with 88 frozen layers) performed the best in terms of accuracy and loss.

## Technologies Used
- Python
- Keras/TensorFlow
- ktrain

## Usage
To use the code in this repository:
1. Clone the repository
   ```
   git clone https://github.com/yourusername/cat-dog-classifier.git
   ```
2. Navigate to the project directory
   ```
   cd cat-dog-classifier
   ```
3. Install the required dependencies
   ```
   pip install -r requirements.txt
   ```
4. Run the Jupyter Notebook
   ```
   jupyter notebook PML.ipynb
   ```
