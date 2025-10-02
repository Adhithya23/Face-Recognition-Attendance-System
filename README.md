# Face-Recognition-Attendance-System



An automated attendance system that uses a webcam to recognize faces and log entries into an Excel file.

---

### Key Features
* **Automated Attendance**: Captures and marks attendance based on facial recognition.
* **Real-time Recognition**: Uses a live webcam feed to identify individuals.
* **Scalable**: Easily add new people by placing their image in the `know_faces` directory.
* **Automated Logging**: Automatically records attendance data (name, date, and time) into an Excel spreadsheet.

---

### Prerequisites
Before you begin, ensure you have the following installed:
* Python (3.6 or higher recommended)
* A working webcam

### Installation
1.  **Clone the repository**:
    ```bash
    git clone [Your Repository URL]
    cd [Your Repository Folder]
    ```

2.  **Install the required libraries**:
    ```bash
    pip install opencv-python face_recognition pandas openpyxl
    ```
    You may also need to install `face_recognition_models` separately:
    ```bash
    pip install git+[https://github.com/ageitgey/face_recognition_models](https://github.com/ageitgey/face_recognition_models)
    ```

3.  **Create the `know_faces` directory**:
    The script looks for a directory named `know_faces`. Create this folder in the same location as `main.py`.

4.  **Add your face image**:
    Place a clear, well-lit image of your face into the `know_faces` directory. The filename **must** be your name. For example, if your name is `Jane Doe`, save the file as `jane_doe.jpg`.

---

### Usage
To run the attendance system, open your terminal or command prompt, navigate to the project directory, and execute the following command:

```bash
python main.py
```
* A window will pop up showing your webcam feed.

* Position your face clearly in the frame.

* Press the spacebar to capture the image.

* The system will then recognize your face and automatically log your attendance in the attendance.xlsx file.

### How it Works
The script follows these simple steps:

1. Loads known face images from the know_faces directory and creates a digital encoding for each face.

2. Uses OpenCV to open your webcam and capture an image when you press the spacebar.

3. Compares the captured face encoding to the known face encodings using the face_recognition library.

4. If a match is found, it records the person's name, the current date, and time into an Excel file using pandas.

### Contributing
Contributions are welcome! If you have suggestions or find a bug, please open an issue or submit a pull request.


