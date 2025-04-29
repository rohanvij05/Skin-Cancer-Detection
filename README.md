File: Untitled Document 1
Page 1 of 2
## Skin Cancer Detection using CNN and AI Medical Assistant
### Project Summary
This project is aimed at building a web-based skin cancer detection system using a
Convolutional Neural Network (CNN). It classifies skin lesions into 7 categories:
- Actinic Keratoses (AKIEC)
- Basal Cell Carcinoma (BCC)
- Benign Keratosis-like Lesions (BKL)
- Dermatofibroma (DF)
- Melanocytic Nevi (NV)
- Vascular Lesions (VASC)
- Melanoma (MEL)
It also includes a **risk prediction module** that evaluates the user's potential risk
based on key factors:
- UV exposure
- Sunscreen use
- Family history
- Skin type
- Presence of moles/freckles
Users interact through a simple **Flask web interface**. The app provides predictions,
medical info, and safety advice.
### Key Features
- Image classification via CNN with custom architecture and BatchNormalization layers.
- Achieved high accuracy (~98.9%) after model tuning.
- Risk calculator based on five user parameters.
- Informative medical descriptions per diagnosis.
- Flask web server to handle inputs and predictions.
- Simple and user-friendly frontend (HTML templates).
- Ready for mobile extension in the future.
### Variables Used
| Variable Name
| Description |
|---------------------|-------------|
| `pic`
| Uploaded image file from user |
| `inputimg`
| Image loaded via PIL for preprocessing |
| `img`
| Numpy array of resized image (28x28x3) |
| `SCD.model`
| Loaded trained CNN model |
| `SCD.classes`
| List of skin cancer class labels |
| `class_ind`
| Index of predicted class |
| `result`
| Final predicted skin cancer class |
| `info`
| Medical information string based on class_ind |
| `risk_score`
| Numerical score from risk calculator |
| `risk_percentage`
| Risk in % calculated from total score |
| `risk_level`
| Risk level string ("High", "Moderate", "Low") |
| `suggestion`
| Personalized safety/medical advice |
### Tech Stack
- Python 3.x
- Flask
- Keras / TensorFlow
- NumPy
- PIL (Image Processing)
- HTML / Jinja2 Templates
- JavaScript (for risk module interaction)
### Folder Structure
```
Skin-Cancer-Detection/
├── app.py
├── skin_cancer_detection.py
├── model.h5
├── wsgi.py
├── templates/
#
#
#
#
Main Flask application
CNN model + class labels
Trained CNN model file
Entry point for deployment servers (Gunicorn, etc.)File: Untitled Document 1
│
│
│
├──
└──
```
├── home.html
├── results.html
└── index.html
requirements.txt
README.md
Page 2 of 2
#
#
#
#
#
Upload form
Output display
Risk calculator page
Dependencies list
Project documentation
### Compilation, Execution & Hardware/Software Requirements
1. **Install Python 3.7+** and all dependencies:
```bash
pip install -r requirements.txt
```
2. **Place the trained CNN model** in the project root (as `best_model.h5`).
3. **Run `wsgi.py`** using Python:
```bash
python wsgi.py
```
4. Open your browser and go to `http://127.0.0.1:5000`
5. Upload an image of a skin lesion and/or use the risk calculator.
**System Requirements:**
- OS: Windows/Linux/Mac
- RAM: Minimum 4 GB (8 GB recommended)
- Python 3.7 or above
- Google Chrome or modern browser
### Future Scope
- Create a full mobile app interface (Android/iOS)
- Enhance chatbot integration for real-time medical Q&A
- Secure patient data using cloud and authentication systems
