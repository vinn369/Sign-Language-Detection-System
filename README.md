# Sign-Language-Detection-System


# Sign Language Detection System

This project is a computer vision-based system for real-time detection and classification of hand gestures representing sign language words. It uses a trained deep learning model to recognize several common sign language gestures and display their meaning.

## Features

- Real-time hand gesture detection** using webcam input.
- Classification of sign language gestures** such as "Hello", "I love you", "No", "Okay", "Please", "Thank you", and "Yes".
- Visual feedback of the detected gesture overlaid on camera input.
- Data collection script to generate training images for new gestures.
- Easily extendable to support additional gestures.

## Project Structure

- `datacollection.py`: Script for collecting gesture data from webcam and saving processed images for model training.
- `test.py`: Main script for running live gesture detection and classification.
- `keras_model.h5`: Pre-trained Keras model for gesture classification.
- `labels.txt`: List of gesture labels/classes supported by the model.

## Requirements and libraries 

- Python 3.x
- OpenCV (`cv2`)
- [cvzone](https://github.com/cvzone/cvzone) for hand tracking and classification modules
- NumPy
- Pre-trained model (`keras_model.h5`)

Install dependencies using pip:

bash :

pip install opencv-python cvzone numpy


## Usage

### 1. Data Collection

To collect new gesture data for training:

bash :
python datacollection.py

- Place your hand showing the desired gesture in front of the webcam.
- Press `s` to save an image of the gesture to the specified folder.

### 2. Gesture Detection

To run real-time detection and classification:

bash :
python test.py

- The system will recognize gestures from the webcam and overlay the detected label on the video stream.
- Press `q` to quit.

### 3. Model & Labels

- The model (`keras_model.h5`) should be trained on images of hand gestures.
- `labels.txt` contains gesture class names (one per line).

## Extending the System

- Collect images for new gestures using `datacollection.py`.
- Retrain the model and update `labels.txt` to include new gesture labels.

## License

[Specify your license here]

## Author

- [vinn369](https://github.com/vinn369)

## Acknowledgements

- [cvzone](https://github.com/cvzone/cvzone) for hand detection and classification utilities.
