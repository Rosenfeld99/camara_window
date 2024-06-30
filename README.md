# Camera Face Verification

This project captures video from your webcam and uses DeepFace to verify if the face in the video matches a reference image. The result is displayed on the video feed in real-time.

## Demo

![Profile manage gif](https://res.cloudinary.com/djwetaeqt/image/upload/v1719787759/github_Images/python-match-person_cjeuuq.jpg)

## Prerequisites

Before you begin, ensure you have met the following requirements:

- You have installed Python 3.6 or higher.
- You have installed the necessary Python packages.
- You have a webcam connected to your computer.

## Installation

1. Clone this repository to your local machine.
2. Navigate to the project directory.
3. Install the required packages by running:

   ```sh
   pip install opencv-python deepface
   ```

## Usage:

1. Place your reference image in the project directory.
2. Open the main.py file and update the following line with the path to your reference image:

   ```sh
    reference_img = cv2.imread("ENTER_YOUR_IMAGE_REFERENCE_URL")

3. Run the script:

   ```sh
   python main.py

4. The script will open a window showing the video feed from your webcam. If the face in the video matches the reference image, "MATCH!" will be displayed on the video feed. Otherwise, "NOT MATCH!" will be displayed.
5. Press the "q" key to stop the script and close the video window.

## Code Explanation

- Imports:
  - threading for running the face verification in a separate thread.
  - cv2 (OpenCV) for capturing and displaying video.
  - DeepFace for face verification.

- Setup:
  - Captures video from the default webcam.
  - Sets the frame width and height.

- Variables:
  - counter for counting frames.
  - face_match for storing the result of face verification.

- Reference Image:
  - Loads the reference image for face verification.

- check_face Function:
  - Runs the face verification using DeepFace in a separate thread.

- Main Loop:
  - Captures frames from the webcam.
  - Every 30 frames, starts a new thread to verify the face in the frame.
  - Displays "MATCH!" or "NOT MATCH!" on the video feed based on the result of the face verification.
  - Pressing the "q" key stops the script and closes the video window.


