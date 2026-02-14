# 👀VisionPartner

<div align="center">

![VisionPartner Logo](https://img.shields.io/badge/VisionPartner-AI%20Navigation%20Assistant-blue?style=for-the-badge)

**Real-Time AI-Powered Navigation Assistant for the Visually Impaired**

[![Flutter](https://img.shields.io/badge/Flutter-02569B?style=flat&logo=flutter&logoColor=white)](https://flutter.dev)
[![TensorFlow](https://img.shields.io/badge/TensorFlow_Lite-FF6F00?style=flat&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/lite)
[![Google Gemini](https://img.shields.io/badge/Google_Gemini-4285F4?style=flat&logo=google&logoColor=white)](https://ai.google.dev)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

[Features](#-features) • [Demo](#-demo) • [Tech Stack](#-tech-stack) • [Architecture](#-architecture) • [Getting Started](#-getting-started) • [Roadmap](#-roadmap)

</div>

---

## 📖 Overview

VisionPartner transforms smartphones into intelligent navigation companions for visually impaired individuals. Unlike traditional object detection apps that simply list what's around you, VisionPartner provides **contextual navigation commands** that tell you exactly how to move safely.

### The Problem

Over 2.2 billion people worldwide with visual impairments face daily challenges navigating even familiar environments:
- White canes detect ground-level obstacles but miss overhead hazards and moving objects
- Guide dogs are expensive ($50,000+), require years of training, and are accessible to less than 2% of those who need them
- Existing apps provide object labels without actionable guidance
- GPS navigation fails indoors and can't detect real-time obstacles

### Our Solution

VisionPartner acts as a **real-time co-pilot**, combining advanced AI scene understanding with practical movement instructions delivered through both **audio and haptic feedback**.

**Instead of saying:** *"Chair detected"*  
**We say:** *"Obstacle on your right — shift left"*

---

## ✨ Features

### 🎯 Core Capabilities

- **🤖 Intelligent Scene Understanding** - Powered by Google Gemini Vision API for contextual awareness
- **⚡ Real-Time Obstacle Detection** - On-device TensorFlow Lite for instant hazard identification
- **🧭 Directional Navigation Commands** - Actionable instructions: "move left", "stop", "stairs ahead"
- **🔊 Multi-Modal Feedback** 
  - Audio guidance via text-to-speech
  - Haptic vibration patterns for silent navigation
- **📶 Offline Core Functionality** - Essential safety features work without internet
- **🎯 Smart Prioritization** - Filters noise, highlights urgent hazards
- **♿ Accessibility-First Design** - Fully operable without visual interface

### 🚨 Hazard Detection

- Stairs and level changes
- Doors and openings
- Moving vehicles
- Pedestrian traffic
- Narrow passages
- Overhead obstacles
- Ground hazards

---

## 🎥 Demo

> **Coming Soon**: Video demonstration of VisionPartner in action

<!--
### Screenshots
[Add screenshots of the app in use]
-->

---

## 🛠️ Tech Stack

### Frontend
- **Flutter** - Cross-platform mobile framework
- **Dart** - Programming language

### AI & Computer Vision
- **Google Gemini Vision API** - Advanced scene understanding and context analysis
- **TensorFlow Lite** - On-device object detection
- **Pre-trained Models** - MobileNet/YOLO optimized for mobile inference

### Device Integration
- **Camera Package** - Real-time video stream capture
- **Flutter TTS** - Text-to-speech engine
- **Vibration Package** - Haptic feedback control

### Development Tools
- **Git & GitHub** - Version control
- **VS Code / Android Studio** - IDEs
- **Flutter DevTools** - Debugging and performance

---

## 🏗️ Architecture

### System Flow

```
📱 Camera Capture → 🤖 Dual AI Processing → 🧠 Navigation Engine → 🔊 Multi-Modal Feedback → 👤 User
```

### Component Breakdown

#### 1️⃣ **Input Layer**
- Continuous camera frame capture
- Real-time video stream processing

#### 2️⃣ **AI Processing Layer**
```
┌─────────────────────────────────────┐
│  Cloud Processing (Gemini Vision)   │  → Rich scene context
│  • Scene understanding              │  → Spatial relationships
│  • Movement patterns                │  → Risk assessment
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│  On-Device (TensorFlow Lite)        │  → Instant detection
│  • Fast obstacle detection          │  → Offline capability
│  • Immediate hazard alerts          │  → Low latency
└─────────────────────────────────────┘
```

#### 3️⃣ **Intelligence Layer**
- **Data Fusion** - Combines cloud + local results
- **Navigation Reasoning Engine**
  - Filters irrelevant objects
  - Prioritizes hazards by urgency
  - Calculates spatial positioning
  - Generates directional commands

#### 4️⃣ **Output Layer**
- **Audio Feedback** - Clear spoken instructions
- **Haptic Feedback** - Directional vibration patterns
  - Left buzz → Move left
  - Right buzz → Move right
  - Long buzz → Stop
  - Rapid pulses → Immediate danger

---

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (3.0 or higher)
- Android Studio / Xcode
- Google Cloud account (for Gemini API)
- Physical device for testing (camera required)

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/visionpartner.git
cd visionpartner
```

2. **Install dependencies**
```bash
flutter pub get
```

3. **Configure API Keys**

Create a `.env` file in the root directory:
```env
GEMINI_API_KEY=your_gemini_api_key_here
```

4. **Run the app**
```bash
flutter run
```

### Building for Production

**Android:**
```bash
flutter build apk --release
```

**iOS:**
```bash
flutter build ios --release
```

---

## 📱 Usage

1. **Launch the app** - VisionPartner starts automatically
2. **Hold phone forward** - Camera should face your walking direction
3. **Listen for guidance** - Audio and vibration will guide you
4. **Adjust settings** - Voice control for volume, speech rate, vibration intensity

### Vibration Patterns

| Pattern | Meaning |
|---------|---------|
| Single left buzz | Shift left |
| Single right buzz | Shift right |
| Long continuous | Stop immediately |
| Rapid pulses | Danger ahead |
| Double buzz | Path clear |

---

## 🗺️ Roadmap

### ✅ Phase 1 - Hackathon MVP (Current)
- [x] Real-time camera processing
- [x] Gemini Vision API integration
- [x] On-device object detection
- [x] Audio + haptic feedback
- [x] Core navigation commands

### 🔄 Phase 2 - User Testing (1-3 months)
- [ ] Beta testing with visually impaired users
- [ ] Performance optimization
- [ ] Battery efficiency improvements
- [ ] Enhanced detection accuracy

### 🎯 Phase 3 - Feature Expansion (3-6 months)
- [ ] Indoor mapping and pathfinding
- [ ] Landmark recognition (ATMs, bus stops, signs)
- [ ] Text and signboard reading (OCR)
- [ ] Crosswalk signal detection
- [ ] Multi-language support

### 🌟 Phase 4 - Advanced Features (6-12 months)
- [ ] Public transit integration
- [ ] Crowd-sourced obstacle database
- [ ] Machine learning personalization
- [ ] Spatial audio guidance (3D sound)

### 🚀 Phase 5 - Long-Term Vision (1-2 years)
- [ ] Smart glasses integration
- [ ] Smart city infrastructure connection
- [ ] Collaborative navigation network
- [ ] AR overlays for low-vision users

---

## 🤝 Contributing

We welcome contributions from the community! Whether you're a developer, designer, or accessibility advocate, there's a place for you.

### How to Contribute

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Areas We Need Help

- 🧪 Testing with visually impaired users
- 🎨 UI/UX improvements for accessibility
- 🤖 ML model optimization
- 🌍 Internationalization and localization
- 📚 Documentation and tutorials
- ♿ Accessibility consulting

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.



---

## 🙏 Acknowledgments

- Google Gemini Team for providing advanced vision AI capabilities
- TensorFlow team for mobile ML frameworks
- Flutter community for excellent cross-platform tools
- Accessibility advocates who provided valuable insights
- All beta testers and contributors

---

## 📞 Contact

**Project Link:** [https://github.com/yourusername/visionpartner](https://github.com/yourusername/visionpartner)

**Email:** your.email@example.com

**Demo Video:** [Coming Soon]

---

## 🌟 Support the Project

If VisionPartner helps you or someone you know, please ⭐ star this repository to help others discover it!

---

<div align="center">

**Making the world navigable for everyone, one step at a time.**

![Built with Flutter](https://img.shields.io/badge/Built_with-Flutter-02569B?style=flat&logo=flutter)
![Powered by AI](https://img.shields.io/badge/Powered_by-AI-FF6F00?style=flat&logo=tensorflow)
![Accessibility First](https://img.shields.io/badge/Accessibility-First-4CAF50?style=flat&logo=accessibility)

</div>
