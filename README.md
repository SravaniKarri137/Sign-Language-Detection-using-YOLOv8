# Sign-Language-Detection-using-YOLOv8
Sign Language Detection using YOLOv8
This repository contains a deep learning-based implementation for sign language recognition using the YOLOv8 object detection model. The project leverages the Ultralytics library to train a custom YOLOv8 model for detecting and classifying various sign language gestures.

Features
Custom Dataset: Trained on a curated dataset of sign language gestures.
YOLOv8: State-of-the-art object detection for fast and accurate predictions.
Real-Time Detection: Detects sign language gestures in real-time through video or image inputs.
Transfer Learning: Fine-tuned pre-trained YOLOv8 model for optimized performance.
Installation
Clone this repository:
bash
Copy code
git clone https://github.com/yourusername/sign-language-detection.git
Navigate to the directory:
bash
Copy code
cd sign-language-detection
Install dependencies:
bash
Copy code
pip install -r requirements.txt
Training the Model
Prepare your dataset in YOLO format (images and corresponding .txt annotation files).
Configure the dataset path in the data.yaml file.
Train the model:
bash
Copy code
yolo task=detect mode=train data=data.yaml model=yolov8n.pt epochs=50 imgsz=640
Evaluation
Run the following command to evaluate the model:

bash
Copy code
yolo task=detect mode=val model=path/to/best.pt data=data.yaml
Inference
Test the trained model on new images or videos:

bash
Copy code
yolo task=detect mode=predict model=path/to/best.pt source=path/to/input
Results
Precision (P): Measures the accuracy of predictions.
Recall (R): Measures the model's ability to identify true positives.
mAP50-95: Mean Average Precision for IoU thresholds ranging from 50% to 95%.
Example Output

Usage
Recognizing sign language gestures in real-time.
Assisting in accessibility technologies for the hearing-impaired community.
Technologies Used
Python 3.10
YOLOv8 (Ultralytics)
OpenCV
Pandas, Matplotlib
Contributing
Feel free to submit issues or pull requests. All contributions are welcome!

License
This project is licensed under the MIT License. See the LICENSE file for details.
