# CNN-Model-for-Vehicle-Recognition
demonstrate how a Convolutional Neural Network (CNN) model can accurately recognize and classify vehicles—cars, bikes, buses, and trucks—using a camera feed. 📷 Learn how deep learning techniques are applied to real-time vehicle detection, with clear visualizations of the CNN architecture and bounding box labels. 🚦

## Features
- Image classification using CNN.
- Data augmentation for better generalization.
- Real-time vehicle recognition via webcam.
- Supports multiple vehicle categories.

## Dataset Structure
Ensure your dataset follows this structure:
```
vehicle_dataset/
│
├── train/
│   ├── cars/
│   ├── trucks/
│   ├── bikes/
│   ├── buses/
│
├── validation/
│   ├── cars/
│   ├── trucks/
│   ├── bikes/
│   ├── buses/
│
├── test/
│   ├── test_image.jpg
```
### Notes:
- Avoid spaces in filenames; use `_` or numbers.
- Store images according to categories in respective folders.

## Installation
Install the required dependencies using:
```sh
pip install tensorflow opencv-python matplotlib keras
```

## Usage
### 1. Train the Model
```python
python train_model.py
```
This script trains the CNN model on the dataset and saves it as `vehicle_model.h5`.

### 2. Test the Model with an Image
```python
test_image.py
```
Modify the `test_image.py` script to load an image and predict its category.

### 3. Real-time Vehicle Recognition
Run the following command to use the model with a webcam:
```python
python live_recognition.py
```
Press `q` to exit the live detection window.

## Model Architecture
The CNN model consists of:
- 3 Convolutional layers
- Max Pooling layers
- Flatten layer
- Fully Connected Dense layers
- Softmax activation for classification

## Training Configuration
- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Metrics: Accuracy
- Epochs: 20
- Batch Size: 32

## Results
After training, the model achieves a high accuracy in classifying vehicles. The accuracy and loss graphs are plotted using `matplotlib`.

## Future Enhancements
- Expand dataset with more vehicle categories.
- Optimize the model for mobile deployment.
- Improve real-time recognition speed.

## For help you can consider this
https://youtu.be/K8olahsjyAc

## Contributors
- Harsh Mogha

## License
This project is licensed under the MIT License.

