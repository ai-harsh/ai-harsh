# 🤖 Xeno AI - Deepfake Detection System

![Xeno AI](https://img.shields.io/badge/Xeno%20AI-Deepfake%20Detection-00f2ff?style=for-the-badge)
![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python)
![Flask](https://img.shields.io/badge/Flask-3.0-green?style=for-the-badge&logo=flask)

A cutting-edge web application powered by AI to detect deepfake images. Xeno AI uses advanced image analysis techniques to identify manipulated or artificially generated images with high accuracy.

## ✨ Features

- 🎯 **Advanced Detection**: Analyze images for deepfake indicators
- ⚡ **Fast Processing**: Get results in seconds
- 🎨 **Modern UI**: Beautiful, responsive interface with animations
- 🔒 **Privacy-Focused**: Images processed locally, not stored
- 📊 **Detailed Analysis**: Comprehensive reports with confidence scores
- 📱 **Mobile-Friendly**: Works on all devices

## 🚀 Quick Start

### Prerequisites

- Python 3.8 or higher
- pip (Python package installer)

### Installation

1. **Clone or navigate to the project directory**
   ```powershell
   cd "C:\Users\HARSH xD\Desktop\new pj"
   ```

2. **Install dependencies**
   ```powershell
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```powershell
   python app.py
   ```

4. **Open your browser**
   Navigate to: `http://localhost:5000`

## 🎮 How to Use

1. **Upload Image**: Drag & drop or browse to select an image (PNG, JPG, JPEG, WEBP)
2. **Analyze**: Click the "Analyze Image" button
3. **View Results**: Get detailed analysis with confidence scores and findings
4. **New Analysis**: Upload another image to analyze more files

## 📁 Project Structure

```
new pj/
├── app.py                  # Flask backend with detection logic
├── requirements.txt        # Python dependencies
├── README.md              # This file
├── static/
│   ├── css/
│   │   └── style.css      # UI styling
│   └── js/
│       └── script.js      # Frontend interactivity
└── templates/
    └── index.html         # Main HTML template
```

## 🔧 Technical Details

### Detection Methods

The current implementation uses multiple image analysis techniques:

- **Color Distribution Analysis**: Detects unusual color patterns
- **Noise Pattern Detection**: Identifies abnormal noise levels
- **Edge Detection**: Analyzes edge smoothing artifacts
- **Compression Analysis**: Checks for manipulation indicators

### Upgrading to ML Models

For production use, you can enhance the detection by:

1. **Using Pre-trained Models**:
   ```python
   # Install TensorFlow/PyTorch
   pip install tensorflow
   # or
   pip install torch torchvision
   ```

2. **Popular Deepfake Detection Models**:
   - MesoNet
   - XceptionNet
   - EfficientNet
   - FaceForensics++

3. **Integration Example**:
   ```python
   import tensorflow as tf
   
   # Load your trained model
   model = tf.keras.models.load_model('path/to/model.h5')
   
   # Update analyze_image_features() in app.py
   def analyze_image_features(image):
       # Preprocess image
       img_array = preprocess_for_model(image)
       
       # Predict
       prediction = model.predict(img_array)
       score = prediction[0][0] * 100
       
       return score, reasons
   ```

## 🎨 Customization

### Changing Colors

Edit [static/css/style.css](static/css/style.css) and modify the CSS variables:

```css
:root {
    --primary-color: #00f2ff;    /* Main accent color */
    --secondary-color: #7b2ff7;  /* Secondary accent */
    --dark-bg: #0a0e27;          /* Background color */
}
```

### Modifying Detection Logic

Update the `analyze_image_features()` function in [app.py](app.py) to customize detection algorithms.

## 📊 API Endpoints

### POST /analyze
Upload and analyze an image for deepfakes.

**Request:**
- Method: POST
- Content-Type: multipart/form-data
- Body: Image file

**Response:**
```json
{
    "result": "AUTHENTIC",
    "confidence": 85.5,
    "deepfake_score": 14.5,
    "status": "safe",
    "reasons": ["Image appears normal"],
    "metadata": {
        "dimensions": "1920x1080",
        "size": "245.67 KB",
        "format": "JPEG"
    }
}
```

## 🛡️ Security Notes

- Maximum file size: 16MB
- Allowed formats: PNG, JPG, JPEG, WEBP
- Files are processed in memory and not saved to disk
- No user data is collected or stored

## 🔮 Future Enhancements

- [ ] Support for video deepfake detection
- [ ] Batch processing multiple images
- [ ] API key system for external access
- [ ] Historical analysis tracking
- [ ] Advanced ML model integration
- [ ] Face-specific deepfake detection
- [ ] Real-time webcam analysis

## 📝 License

This project is open source and available for personal and educational use.

## 🤝 Contributing

Contributions are welcome! To improve Xeno AI:

1. Add better detection algorithms
2. Improve the UI/UX
3. Add new features
4. Fix bugs
5. Update documentation

## 📧 Support

For issues or questions, please open an issue in the project repository.

## 🌟 Acknowledgments

- Built with Flask and modern web technologies
- Inspired by the need for accessible deepfake detection tools
- Designed to promote digital media authenticity

---

**Made with ❤️ by HARSH xD | Powered by Xeno AI**

*Stay vigilant in the age of synthetic media!*
