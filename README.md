# README.md

## Praxis Project: Improving Object Detection for a Robotic Arm

### Project Description

This project focuses on enhancing the object detection capabilities of a small robotic arm (Niryo Ned2) designed to pick up chocolate bars. The existing application struggles with varying lighting conditions, leading to confusion between different brands of chocolate bars. The goal is to train a more robust object detection model compared to the manufacturer's provided classification model, which includes image processing for detecting chocolate bars.

### Key Objectives

1. **Data Preparation**:

   - Utilize existing training data from the manufacturer's GitHub repository.
   - Automate the labeling process for object detection using provided scripts.
   - Augment the dataset using techniques like Data Augmentation and Domain Randomization to improve robustness under different lighting conditions (e.g., brightness, noise, background color).

2. **Model Selection**:

   - Implement the YOLOv8 model (from Ultralytics) for object detection, as it is well-suited for this task.
   - Explore object segmentation as an alternative to improve the determination of the chocolate bar's position, which is crucial for the robotic arm's gripper control.

3. **Training and Evaluation**:
   - Train the YOLOv8 model using the prepared dataset.
   - Compare the performance of the trained YOLOv8 model with the manufacturer's model and a custom-built model.
   - Evaluate the models based on classification accuracy and bounding box mean Average Precision (mAP).

### Project Workflow

1. **Data Handling**:

   - Uploaded the dataset to Roboflow for preprocessing.
   - Applied Data Augmentation techniques (e.g., Albumentations) to increase dataset diversity.
   - Split the dataset into training, validation, and test sets.

2. **Model Training**:

   - Trained the YOLOv8 model using the augmented dataset.
   - Performed validation and testing to assess the model's performance.

3. **Comparison and Evaluation**:
   - Tested the manufacturer's model and the custom-trained model on the same test data.
   - Ranked the models based on their performance metrics.

### Tools and Technologies

- **Roboflow**: For dataset augmentation and management.
- **YOLOv8**: For object detection, leveraging Ultralytics' implementation.
- **Albumentations**: For image augmentation to enhance model robustness.
- **Python and Jupyter Notebook**: For scripting and model training.

### Results

- The project successfully improved the object detection model's accuracy under varying lighting conditions.
- The YOLOv8 model demonstrated superior performance compared to the manufacturer's model, particularly in handling diverse lighting scenarios.

### Future Improvements

- Collect additional training data using a camera to further enhance the model's robustness.
- Experiment with more advanced augmentation techniques or alternative models (e.g., segmentation-based approaches) for better accuracy.

### Repository Structure

- `praxis_project.ipynb`: Jupyter notebook containing the project's code, including data preprocessing, model training, and evaluation.
- `README.md`: This file, providing an overview of the project.
- Dataset and model files (if included separately).

### How to Use

1. Clone the repository.
2. Open the Jupyter notebook (`praxis_project.ipynb`) to explore the code and results.
3. Follow the instructions in the notebook to replicate the training and evaluation process.

### Acknowledgments

- Thanks to Niryo Robotics for providing the initial dataset and application framework.
- The Ultralytics team for the YOLOv8 implementation.
