#Image and Video Dehazing with Object Detection
This project focuses on applying dehazing techniques to images and videos to improve visibility under various environmental conditions such as fog, rain, darkness, heavy sunlight, and smoke. Following dehazing, the YOLOv8m model is used to detect objects in the processed images and videos.

##Table of Contents
Introduction
Installation
Usage
Training
Results
Contributing
License
Introduction
The project consists of two main parts:

##Image and Video Dehazing: Enhances images and videos to improve visibility under adverse environmental conditions using OpenCV and NumPy.
Object Detection: Uses the YOLOv8m model to detect objects in the dehazed images and videos.
##Installation
Clone the repository:

git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name

Create a conda environment and install dependencies:

conda create -n dehaze-detection python=3.8
conda activate dehaze-detection
pip install -r requirements.txt
Usage
##Image and Video Dehazing
The Image_Videodehazing.py script processes images and videos to remove haze caused by environmental conditions.

python Image_Videodehazing.py --input path_to_input_file --output path_to_output_file
##Object Detection
After dehazing, the YOLOv8m model is used for object detection. The detection parameters are defined in data.yaml.


python detect.py --weights yolov8m.pt --source path_to_dehazed_file --data data.yaml
Training
To train the YOLOv8m model with your dataset, follow these steps:

Ensure your dataset is properly formatted and listed in classes.txt.

Update the data.yaml file with your dataset path and other configurations.

Train the model using the following command:


python train.py --img-size 640 --batch-size 16 --epochs 200 --data data.yaml --weights yolov8m.pt
The training process was configured for 200 and then 500 epochs but stopped early at 35 and 65 epochs respectively based on early stopping criteria.

##Results
The trained model was evaluated on a random test dataset and achieved an F1 score ranging from 0.81 to 0.97.

##Contributing
Contributions are welcome! Please read the CONTRIBUTING.md for guidelines.

##License
This project is licensed under the MIT License - see the LICENSE file for details.
