~Vehicle Speed Detection System using Python 
This project detects multiple vehicles from a video feed and estimates their speeds in real-time using object tracking and motion analysis. It uses OpenCV, dlib, and Haar Cascade Classifiers to track moving cars, calculate speed, and overlay results directly on the video frame.

~Project Structure
bash
Copy
Edit
📂 Vehicle-Speed-Detection/
├── README.md           # Project documentation
├── cars.mp4            # Input video file
├── outpy.avi           # Output video with speed overlay (auto-generated)
├── myhaar.xml          # Haar cascade classifier for vehicle detection
└── speed_detection.py  # Main Python script
~Technologies Used
Python

OpenCV (Image processing, object detection)
dlib (Object tracking)
Haar Cascade Classifier (Vehicle detection)
Math & Time Modules (Speed estimation)

~Features
Detects multiple moving vehicles in a video
Tracks each vehicle using dlib correlation tracker
Estimates vehicle speed using pixel displacement and calibrated PPM (pixels per meter)
Displays speed in real-time on each vehicle
Saves processed video with bounding boxes and speed overlay

~How Speed is Calculated
Car is detected using Haar Cascade (myhaar.xml)
Tracked using dlib's correlation tracker
Displacement is calculated between two positions

Speed formula used:

bash
Copy
Edit
speed (km/h) = (distance_moved_in_pixels / pixels_per_meter) × fps × 3.6
~How to Run
Make sure Python 3.x is installed

Install dependencies:

bash
Copy
Edit
pip install opencv-python dlib
Place your input video (cars.mp4) and Haar XML file (myhaar.xml) in the same directory

Run the script:

bash
Copy
Edit
python speed_detection.py
Press ESC to stop the video

~Output

The script will generate a file named outpy.avi with bounding boxes and vehicle speed annotations
Real-time display of each car’s speed in km/h

~Use Cases

Traffic monitoring
Vehicle speed detection for surveillance
Smart city traffic systems
Real-time transport analytics



