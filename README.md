# Pulse Monitor from Phone Video ❤️

A browser-based experimental application that estimates heart rate (BPM) using a smartphone camera. The project explores two camera-based measurement approaches: **Finger Photoplethysmography (PPG)** and **Remote Photoplethysmography (rPPG)**.

The application processes camera video, extracts variations in pixel intensity, and applies basic signal-processing techniques to estimate pulse rate.

The goal of this project is to explore how accessible smartphone cameras and web technologies can be used for contact-based and contactless pulse monitoring.

## ✨ Features

- **Finger Mode (PPG):** Estimates pulse rate using light variations captured when a fingertip covers the rear camera and flash.
- **Face Mode (Experimental rPPG):** Estimates pulse rate using subtle changes in facial skin colour captured by the front camera.
- **Camera Switching:** Switch between rear and front camera modes.
- **30-Second Measurement:** Captures video samples during a measurement session.
- **Real-Time Signal Visualization:** Displays a filtered pulse waveform and frequency spectrum.
- **Heart Rate Estimation:** Displays estimated beats per minute (BPM).
- **Signal Quality Indicator:** Provides an experimental signal-quality score.
- **Measurement History:** Stores recent measurement results in the browser.
- **CSV Export:** Download measurement history for further analysis.
- **Responsive Interface:** Designed to work on desktop and mobile browsers.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Responsive user interface |
| JavaScript | Camera handling and application logic |
| MediaDevices API | Access to smartphone cameras |
| Canvas API | Image sampling and signal visualization |
| Local Storage | Saving measurement history |
| Signal Processing | Filtering, frequency analysis and pulse estimation |

## 🔬 How It Works

### 1. Finger Mode – PPG

Photoplethysmography (PPG) is an optical technique used to detect changes in blood volume beneath the skin.

In this project:
1. Place your fingertip over the rear smartphone camera and flash.
2. The application captures video frames.
3. It calculates average red-channel intensity from a selected image region.
4. Changes in pixel intensity are processed to extract a pulse-related signal.
5. The application estimates heart rate in BPM.

### 2. Face Mode – Experimental rPPG

Remote photoplethysmography (rPPG) explores pulse estimation without direct physical contact.

In this project:
1. Select Face Mode and position your face in front of the camera.
2. The application captures video frames under steady lighting.
3. It samples average green-channel intensity from a predefined facial region.
4. The signal is filtered and analysed to estimate pulse rate.

**Note:** This is a simplified experimental implementation. It does not perform facial recognition or automatic face detection. The selected region is fixed, so positioning and lighting can significantly affect results.

## 🚀 Getting Started

### Option 1: Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR-USERNAME/pulse-monitor.git
   ```

2. Open the project folder:

   ```bash
   cd pulse-monitor
   ```

3. Start a local development server or open the project through an HTTPS-enabled hosting service.

4. Open the application in your browser and allow camera access.

**Important:** Camera access through the browser generally requires HTTPS or localhost. Opening the HTML file directly may not provide camera access on mobile devices.

### Option 2: Run Using GitHub Pages

The application can be hosted using GitHub Pages.

1. Open your repository on GitHub.
2. Navigate to **Settings → Pages**.
3. Under Build and deployment, select **Deploy from a branch**.
4. Select the `main` branch and `/ (root)` folder.
5. Save the settings.
6. Open the published GitHub Pages URL.

## 📱 How to Use

1. Open the application using Chrome or another supported modern browser.
2. Select **Finger** or **Face** mode.
3. Position your finger or face according to the selected mode.
4. Press **Start 30 s measurement**.
5. Allow camera access when prompted.
6. Stay still and maintain consistent lighting throughout the measurement.
7. Review the estimated BPM, signal quality, waveform and frequency spectrum.
8. View previous measurements in the history section.
9. Export results using the **Download CSV** option.

## 🔐 Privacy

- Camera access is requested only when the user starts a measurement.
- Image sampling and signal processing are performed locally in the browser.
- This implementation does not include a backend service for uploading camera frames.
- Measurement history is stored in the browser's local storage.
- Clearing browser site data may remove saved measurement history.

## ⚠️ Limitations and Disclaimer

This project is an educational prototype developed for experimentation and learning.

- It is not a certified medical device.
- It must not be used for diagnosis, treatment or medical decision-making.
- Estimated BPM values may differ from actual heart rate.
- Lighting, movement, camera quality, skin positioning and device capabilities can affect results.
- Face mode is particularly experimental and has not been clinically validated.
- Flashlight support depends on the smartphone and browser.
- Signal-quality scores are approximate and should not be interpreted as clinical confidence measurements.

For reliable health measurements, use an appropriate validated medical device.

## 🗺️ Future Improvements

Potential areas for further development include:

- Automatic face detection and facial region tracking.
- Improved rPPG signal extraction and noise reduction.
- More robust signal-quality assessment.
- Better handling of camera switching across mobile devices.
- Comparison against reference pulse measurement devices.
- Improved measurement accuracy and validation.
- Additional visualization and measurement analytics.

## 🤝 Contributing

Contributions, suggestions and feedback are welcome!

If you find a bug or have an idea for improvement:

1. Fork this repository.
2. Create a new feature branch.
3. Commit your changes.
4. Open a Pull Request describing your improvements.

## 👨‍💻 Author

**Bilal Inamdar**

GitHub: [@rumaan-inamdar](https://github.com/rumaaan-inamdar)

Project: [Pulse Monitor](https://github.com/rumaaan-inamdar/pulse-monitor)

---

⭐ If you find this project interesting, consider giving the repository a star!

*Built as an educational exploration of smartphone-based pulse monitoring, web technologies and signal processing.*
