# SIGNALWARDEN

**RF Signal Classifier and Visual Interface**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Linux-lightgrey)](https://github.com/ryanauscoll/SIGNALWARDEN)
[![Status](https://img.shields.io/badge/status-in%20development-orange)](https://github.com/ryanauscoll/SIGNALWARDEN)

---

## 🔍 Overview

SIGNALWARDEN is a real-time RF signal monitoring and classification tool that leverages RTL-SDR hardware to collect local radio signals, generates detailed spectrograms, and classifies them using advanced neural network models. The application features a sleek Streamlit dashboard that provides real-time visualization and comprehensive session logging capabilities.

## 🧠 Features

- **📡 RTL-SDR Signal Acquisition** - Real-time radio frequency signal capture
- **🖼 Spectrogram Generation** - Automated spectrogram creation and storage
- **🧠 PyTorch-based Classification** - Neural network-powered signal identification
- **🧾 Signal Metadata Logging** - Comprehensive data tracking and analysis
- **📊 Live Dashboard Interface** - Interactive Streamlit-based GUI
- **🔄 Real-time Processing Loop** - Continuous signal monitoring and classification

## ⚙️ Requirements

### Hardware
- RTL-SDR device (e.g., RTL-SDR Blog V3)
- Compatible antenna for target frequency ranges

### Software
- **Python 3.9+**
- **librtlsdr** library
  ```bash
  # macOS
  brew install librtlsdr
  
  # Ubuntu/Debian
  sudo apt-get install librtlsdr-dev
  
  # CentOS/RHEL
  sudo yum install rtl-sdr-devel
  ```

### Python Dependencies

Install all required packages using:

```bash
pip install -r requirements.txt
```

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/ryanauscoll/SIGNALWARDEN.git
cd SIGNALWARDEN
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch the Dashboard
```bash
streamlit run src/gui/dashboard.py
```

### 4. Start Real-time Classification
```bash
python3 src/realtime_signal_listener.py
```

### 5. (Optional) Train Custom Model
```bash
python3 src/classifier/train_model.py
```

## 📁 Project Structure

```
SIGNALWARDEN/
├── assets/
│   └── signalwarden_logo.png
├── data/
│   └── spectrograms/
├── models/
│   └── signal_classifier.pth
├── src/
│   ├── classifier/
│   │   ├── model.py
│   │   ├── train_model.py
│   │   └── __init__.py
│   ├── gui/
│   │   └── dashboard.py
│   ├── utils/
│   │   ├── spectrogram.py
│   │   └── __init__.py
│   ├── realtime_signal_listener.py
│   └── __init__.py
├── requirements.txt
└── README.md
```

## 🛰 Use Cases

- **RF Situational Awareness** - Monitor local electromagnetic spectrum activity
- **Passive Signal Reconnaissance** - Identify and catalog radio transmissions
- **Educational Demonstrations** - Teaching wireless and cyber-physical systems concepts
- **ML Pipeline Preprocessing** - Generate training data for offline RF machine learning projects

## 🔮 Future Improvements

- **Database Backend** - SQLite or MongoDB integration for persistent data storage
- **Expanded Signal Classes** - Additional pretrained classification categories
- **Enhanced Visualizations** - Waterfall displays and real-time FFT plots
- **IQ Recording & Playback** - Raw signal capture and analysis capabilities
- **Mobile Support** - GPS metadata integration for location-aware monitoring

## 🤝 Contributing

We welcome contributions from the community! Areas where help is especially appreciated:

- **Model Accuracy** - Improving classification performance and adding new signal types
- **GUI Enhancements** - Dashboard features and user experience improvements
- **SDR Compatibility** - Support for additional software-defined radio hardware
- **Documentation** - Code comments, tutorials, and usage examples

To contribute:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**Ryan Auscoll** - [@ryanauscoll](https://github.com/ryanauscoll)

---

*Built with ❤️ for the RF and SDR community*
