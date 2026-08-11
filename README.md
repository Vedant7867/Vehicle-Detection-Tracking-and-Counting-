# Vehicle Detection, Tracking, and Counting

A simple computer vision project that detects vehicles in a video, tracks them frame-by-frame, and counts them based on which direction they are traveling.

---

##  Tools Used
* **Python**
* **YOLOv11** (for object detection)
* **OpenCV** (for drawing lines and processing video frames)

---

##  Features
* **Vehicle Detection:** Identifies vehicles like cars, trucks, and buses using YOLOv11.
* **Real-Time Tracking:** Tracks each vehicle across frames with unique IDs.
* **Two-Way Counting:** Uses virtual **Red** and **Blue** lines to count vehicles moving up or down.
* **Type-Based Count:** Keeps separate counters for each type of vehicle (e.g., Car: 5, Truck: 2).

---

##  How It Works

1. **Detect & Track:** The model scans each frame, detects vehicles, and assigns a unique ID to each one.
2. **Draw Lines:** Two imaginary lines (Red and Blue) are placed on the screen.
3. **Check Movement:** 
   * **Moving Down:** Crosses the **Red line first**, then the **Blue line**.
   * **Moving Up:** Crosses the **Blue line first**, then the **Red line**.
4. **Update Counter:** Once a vehicle crosses both lines, its count is updated on the screen.

---

##  How to Run

### 1. Install Libraries
```bash
pip install opencv-python pandas ultralytics
