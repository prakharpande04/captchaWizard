🧠 CAPTCHA Text Recognition
This project aims to develop a deep learning system to recognize alphanumeric text from CAPTCHA images using a ResNet-based neural network. The ultimate goal is to automate CAPTCHA decoding with high accuracy and reliability.

🔍 Project Overview
📸 Uses ResNet50 architecture (pre-trained on ImageNet) as the base feature extractor.

🖼️ Designed for CAPTCHA images resized to (200×50) pixels.

🔢 Outputs a 6-character prediction corresponding to the text in the CAPTCHA image.

🧮 Trained using Mean Squared Error (MSE) loss — a regression-based approach to predict character indices.

📁 Dataset
The dataset is divided into three subsets:

🧪 Training Set: 6,000 CAPTCHA images used for training the model.

🧯 Validation Set: 2,000 images used during model validation while training.

🧾 Test Set: 2,000 images used for evaluating final model performance.

Each image is accompanied by a ground-truth label, representing the actual CAPTCHA text.

🧱 Model Architecture

Layer Type	Configuration
Base Model	ResNet50(weights='imagenet', include_top=False)
Pooling Layer	Global Average Pooling 2D
Dense Layer 1	512 Units, Activation: ReLU
Dense Layer 2	256 Units, Activation: ReLU
Output Layer	6 Units (One per character index)
⚙️ Current Status
✅ Built using TensorFlow / Keras.

🔧 Currently uses a basic ResNet-based model.

📉 Achieved promising results with:

Training Loss: 0.0719

Test Loss: 0.1021

🛠️ Next Steps:

Improve accuracy with better decoding strategy (e.g., CTC Loss).

Automate the prediction workflow and pipeline.

Explore augmentations and sequence models (e.g., CRNN).

