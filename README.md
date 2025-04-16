# Face Mask Detection

This project uses deep learning and computer vision to detect whether a person is wearing a face mask in real-time from a webcam feed. The application uses a pre-trained MobileNetV2 model fine-tuned on a face mask detection dataset.

## Requirements

Make sure to have the following dependencies installed:

- Python 3.x
- OpenCV (`cv2`)
- TensorFlow 2.x
- imutils
- numpy

You can install these dependencies by running:

```bash
pip install opencv-python tensorflow imutils numpy
How to Run the Project
Download and Prepare the Model:

Make sure you have the trained mask detection model (mask_detector.model) saved in the project directory. If not, train the model first using the train_mask_detector.py script.

Run the Face Mask Detection:

Use the following command to run the detect_mask_video.py script and start detecting masks from your webcam.

bash
Copy
Edit
How It Works:

The application uses a pre-trained face detector to locate faces in each frame of the video feed.

The detected face regions are passed to the mask detection model, which classifies whether the face has a mask or not.

The results (Mask/No Mask) are displayed on the frame in real-time with bounding boxes and labels.

Exit the Video Feed:

Press q on your keyboard to stop the video feed and exit the program.
Face Mask Detection Model
The model used in this project is a fine-tuned MobileNetV2 model. It classifies whether a detected face is wearing a mask or not. The model was trained using the following dataset:

Face Mask Dataset

Training the Model
If you wish to train your own model, you can use the train_mask_detector.py script. Make sure to have the dataset in the correct format and train the model before running the detection.

Troubleshooting
Issue: "The model file doesn't load correctly."

Solution: Make sure the mask_detector.model file is in the correct directory and that it is a valid Keras .h5 or .keras model.

Issue: "Error with video stream."

Solution: Ensure your webcam is connected and accessible by OpenCV.
