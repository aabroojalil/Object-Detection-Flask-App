# Object Detection Flask App

This is a Flask application for performing object detection on uploaded images. It utilizes the OpenCV library to detect objects in images using the MobileNetSSD model. Detected objects are then highlighted with bounding boxes and labeled with their class and confidence.

## Requirements

- Python 3.x
- Flask
- OpenCV

## Installation

1. Clone the repository or download the source code.
2. Install the required dependencies using the following command:
   ```
   pip install flask opencv-python
   ```

## Usage

1. Run the Flask application by executing the following command in the project directory:
   ```
   python app.py
   ```
2. Access the application by opening your web browser and navigating to `http://localhost:5000`.
3. Upload an image file (supported formats: jpg, png, jpeg) using the provided form.
4. After the image is uploaded and processed, the detected objects will be displayed on the page along with the original and processed images.

## Configuration

The following configuration options can be modified in the `app.py` file:

- `UPLOAD_FOLDER`: The folder where uploaded images will be saved.
- `DOWNLOAD_FOLDER`: The folder where processed images will be saved.
- `ALLOWED_EXTENSIONS`: A set of allowed file extensions for image uploads.
- `SECRET_KEY`: A secret key used for session management.
- `MAX_CONTENT_LENGTH`: The maximum allowed file size for uploads in bytes.

## Notes

- The MobileNetSSD model files (`MobileNetSSD_deploy.prototxt.txt` and `MobileNetSSD_deploy.caffemodel`) should be present in the `ssd` directory.
- The confidence threshold for object detection is set to 0.60. You can adjust this value in the `detect_object` function.
- The detected objects are drawn as bounding boxes with labels on the processed image. The class labels and colors are defined in the `CLASSES` and `COLORS` variables, respectively.

Feel free to explore and modify the code to suit your needs!


