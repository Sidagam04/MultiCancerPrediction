# 🧬 Multicancer Detection Web App: An Enhanced Project Overview

## 📖 Project Summary

This project presents a **Multicancer Detection System** using deep learning to classify four types of cancer: brain, lung, colon, and kidney. The system leverages a combination of custom Convolutional Neural Networks (CNNs) and the powerful ResNet50 architecture. The models were trained in Google Colab for efficient GPU acceleration and are now integrated into a user-friendly Flask-based web application. Users can upload an image and receive a real-time prediction, making this a practical tool for preliminary medical image analysis.

-----

## 🚀 Key Features and Enhancements

  * **Diverse Model Architecture**: The system utilizes both a custom CNN for brain tumor detection and the robust **ResNet50** pre-trained model for lung, colon, and kidney cancer, allowing for high accuracy on complex medical image data.
  * **High-Accuracy Predictions**: The models have achieved impressive accuracy scores, with colon cancer detection at **99.8%**, and brain, lung, and kidney cancer detection all above **98%**.
  * **Intuitive User Interface**: The web app, built with Flask, HTML, CSS, and JavaScript, provides a clean interface for users to upload images and select the specific cancer type they want to analyze.
  * **Scalable Architecture**: The clear separation of model training (Colab notebooks) and the web application (Flask) in the project structure facilitates easier management, updates, and future scaling.
  * **Robust File Handling**: The Flask backend uses secure methods like `secure_filename` and unique identifiers (`uuid`) to safely handle user-uploaded images, preventing potential security vulnerabilities.

-----

## 📂 Project Structure

```
├── colab_notebooks/                # Notebooks for model training
│   ├── brain_cancer.ipynb
│   ├── lung_cancer.ipynb
│   ├── colon_cancer.ipynb
│   └── kidney_cancer.ipynb
|
├── models/                        # Trained models in .h5 format
│   ├── brain_tumor_model.h5
│   ├── lung_cancer_model.h5
│   ├── colon_cancer_model.h5
│   └── kidney_cancer_model.h5
|
├── app.py                         # The main Flask application backend
|
├── templates/                     # Frontend HTML files
│   └── index.html                 # Main page for image upload and results
|
├── static/                        # CSS, JS, and image assets
│   ├── css/
│   ├── js/
│   └── images/
|
├── requirements.txt               # List of all Python dependencies
└── README.md                      # Comprehensive project documentation
```

-----

## ⚙️ Tech Stack

  * **Model Training**: Python, TensorFlow, Keras, OpenCV.
  * **Web Application**: **Flask** for the backend, **HTML/CSS/JavaScript** for the frontend, and **Werkzeug** for secure file uploads.

-----

## ▶️ How to Use

### **1. Model Training (Google Colab)**

1.  Open and run the notebooks located in the `colab_notebooks/` directory to train each cancer detection model.
2.  After training, save the models as `.h5` files and download them.
3.  Place the downloaded `.h5` model files into the `models/` folder.

### **2. Web Application Setup (Local Machine)**

1.  Clone the repository and navigate into the project directory:
    `git clone https://github.com/your-username/multicancer-detection-webapp.git`
    `cd multicancer-detection-webapp`
2.  Install all necessary dependencies by running the command:
    `pip install -r requirements.txt`
3.  Ensure the `.h5` model files are correctly placed in the `models/` folder.
4.  Launch the Flask application:
    `python app.py`
5.  Open your web browser and go to `http://127.0.0.1:5000` to access the application.
6.  Upload a medical image, select the corresponding cancer type, and click the button to get an instant prediction.

-----

## 🔮 Future Work & Deployment

  * **Full-Stack Deployment**: Deploy the web app on a cloud platform like AWS, Google Cloud Platform (GCP), or Heroku for global accessibility and scalability.
  * **Enhanced UI/UX**: Rebuild the frontend using modern frameworks like React.js or Streamlit to create a more dynamic and interactive user experience.
  * **Secure Data Management**: Explore the integration of **blockchain technology** to provide a secure, immutable, and decentralized system for storing patient medical records and diagnostic data.
  * **Unified Ensemble Model**: Develop a single, unified deep learning model that can detect all four cancer types from a single image input, further streamlining the diagnostic process.
