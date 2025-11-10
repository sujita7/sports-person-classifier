# Sports Person Classifier

A machine learning web application that classifies images of sports celebrities using OpenCV and SVM algorithm. The model is trained to recognize 15 Indian cricket players with an accuracy of 87.8%.

## 🏏 Players Recognized

- Virat Kohli
- Rohit Sharma
- K L Rahul
- Shubman Gill
- Hardik Pandya
- Jasprit Bumrah
- Mohammed Shami
- Mohammed Siraj
- Ravichandran Ashwin
- Ravindra Jadeja
- Axar Patel
- Kuldeep Yadav
- Rishabh Pant
- Suryakumar Yadav
- Yuzvendra Chahal

## 🚀 Features

- **Image Classification**: Upload images and get instant classification results
- **Face Detection**: Uses OpenCV Haar cascades for face detection
- **Wavelet Transform**: Applies wavelet transforms for feature extraction
- **Web Interface**: Clean and responsive web interface for easy interaction
- **REST API**: Backend API for image classification

## 🛠️ Tech Stack

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Flask (Python)
- **Machine Learning**: OpenCV, Scikit-learn, NumPy
- **Image Processing**: Pillow, Wavelet transforms
- **Deployment**: Vercel

## 📋 Prerequisites

- Python 3.7+
- pip (Python package manager)

## 🚀 Quick Start

### Local Development

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/sports-person-classifier.git
   cd sports-person-classifier
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   python main.py
   ```

4. **Open your browser**
   Navigate to `http://localhost:5000`

### Deployment on Vercel

1. **Install Vercel CLI**
   ```bash
   npm i -g vercel
   ```

2. **Deploy**
   ```bash
   vercel
   ```

## 📁 Project Structure

```
├── main.py              # Flask application entry point
├── util.py              # Utility functions for image processing
├── wavlet.py            # Wavelet transform implementation
├── requirements.txt     # Python dependencies
├── vercel.json          # Vercel deployment configuration
├── templates/           # HTML templates
│   └── app.html
├── static/              # CSS, JS, and image assets
│   ├── app.css
│   ├── app.js
│   └── images/
├── model/               # ML models and test images
│   ├── opencv/          # Haar cascades
│   └── test_images/
└── server/artifacts/    # Saved model and class dictionary
```

## 🔧 API Endpoints

- `GET /` - Serve the main application
- `POST /classify_image` - Classify uploaded image

## 🎯 How It Works

1. **Image Upload**: User uploads an image through the web interface
2. **Face Detection**: OpenCV detects faces in the image
3. **Feature Extraction**: Wavelet transforms extract features from detected faces
4. **Classification**: SVM model classifies the image based on extracted features
5. **Result Display**: Classification results are displayed to the user

## 📊 Model Performance

- **Accuracy**: 87.8%
- **Algorithm**: Support Vector Machine (SVM)
- **Features**: Raw pixels + Wavelet coefficients
- **Image Size**: 32x32 pixels

## 🚀 Deployment

The application is deployed on Vercel and can be accessed at: [Your Vercel URL]

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.

## 🙏 Acknowledgments

- OpenCV community for computer vision tools
- Scikit-learn for machine learning algorithms
- Vercel for hosting platform
