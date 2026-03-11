#  MoodMate

An interactive mood detection application that uses AI to recognize your facial expressions and responds with matching sounds. Perfect for learning about computer vision, emotion recognition, and multimedia feedback systems.

## Overview

MoodMate captures video from your webcam, analyzes your facial expression in real-time, detects your current emotion (happy, sad, angry, neutral, or surprised), and plays audio clips that correspond to your mood. It's a fun, interactive demo that combines **computer vision**, **deep learning**, and **audio processing**.

---

##  Features

- **Real-time Emotion Detection** – Uses DeepFace AI model for accurate facial expression analysis
- **Automatic Audio Response** – Plays corresponding sound clips for detected emotions
- **Webcam Integration** – Seamless video capture from your default webcam
- **Emotion Cooldown** – Prevents audio spam; only plays sounds when emotion changes
- **Lightweight & Modular** – Easy to customize emotions, sounds, or detection settings
- **Educational Demo** – Learn how computer vision + AI works with practical, interactive code

---

##  Requirements

- Python 3.7+
- Webcam/camera device
- Dependencies listed in requirements section

---

##  Installation

### 1. Clone or Download
```bash
cd moodmate
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

Required packages:
- `opencv-python` – Video capture and image processing
- `deepface` – Deep learning-based emotion detection
- `pygame` – Audio playback

Or install manually:
```bash
pip install opencv-python deepface pygame
```

---

##  Quick Start

### Run the Application
```bash
python mood.py
```

The application will:
1. Open your webcam
2. Display video feed with emotion detection
3. Play audio clips when emotions are detected
4. Run continuously until you close the window

### Stop the Application
Press `q` or close the window to exit.

---

##  Project Structure

```
moodmate/
├── mood.py              # Main application (DeepFace-based)
├── mood1.py             # Alternative implementation
├── mood3.py             # Alternative implementation
├── mood4.py             # Alternative implementation
├── sounds/              # Audio files directory
│   ├── happy.mp3       # Happy emotion sound
│   ├── sad.mp3         # Sad emotion sound
│   ├── angry.mp3       # Angry emotion sound
│   ├── neutral.mp3     # Neutral emotion sound
│   ├── surprise.mp3    # Surprise emotion sound
│   └── horror.mp3      # Additional sound effect
└── README.md           # This file
```

---

##  How It Works

### Step-by-Step Process

1. **Video Capture** – OpenCV captures frames from your webcam at real-time speed
2. **Face Detection** – Frames are analyzed for face(s)
3. **Emotion Analysis** – DeepFace processes detected faces and classifies emotions:
   - 😊 Happy
   - 😢 Sad
   - 😠 Angry
   - 😶 Neutral
   - 😮 Surprise
4. **Audio Playback** – Python's pygame plays the corresponding sound file
5. **Cooldown Management** – 5-second cooldown prevents repeated sounds for the same emotion

### Emotion-Sound Mapping

| Emotion  | Sound File       |
|----------|-----------------|
| Happy    | `sounds/happy.mp3`     |
| Sad      | `sounds/sad.mp3`       |
| Angry    | `sounds/angry.mp3`     |
| Neutral  | `sounds/neutral.mp3`   |
| Surprise | `sounds/surprise.mp3`  |

---

## 🔧 Customization

### Change Sound Files
Edit the `emotion_sounds` dictionary in `mood.py`:
```python
emotion_sounds = {
    "happy": "sounds/your_happy_sound.mp3",
    "sad": "sounds/your_sad_sound.mp3",
    # ... etc
}
```

### Adjust Cooldown Time
Modify the `cooldown` variable in `mood.py`:
```python
cooldown = 3  # Play sounds every 3 seconds instead of 5
```

### Use Different Implementations
Try alternative versions:
- `python mood1.py`
- `python mood3.py`
- `python mood4.py`

---

##  Troubleshooting

### "Webcam not accessible" Error
- Check if another application is using your webcam
- Verify camera permissions (especially on macOS/Linux)
- Try unplugging and replugging the camera device

### No Audio Output
- Verify sound files exist in the `sounds/` directory
- Check system volume settings
- Test audio with: `pygame.mixer.Sound("sounds/happy.mp3").play()`

### DeepFace Download Issues
- First run may download the model (~300MB)
- Ensure stable internet connection during first execution
- Models are cached locally after initial download

### High CPU Usage
- Lower webcam resolution in OpenCV settings
- Increase cooldown time to reduce detection frequency
- Close other applications

---


---

##  Ideas for Extension

- Add more emotions or facial landmarks detection
- Implement emotion history/analytics
- Add GUI with emotion statistics display
- Create different audio responses based on confidence levels
- Add video recording with emotion timestamps
- Deploy as a web app using Flask/FastAPI

---

##  Contributing

Found a bug or have ideas? Feel free to enhance the project!

---

##  Author
- **Anoop Tripathi**
- **B.Tech in Artificial Intelligence and Data Science**
-**IIT Patna**

**Happy mood detecting! 😊**
