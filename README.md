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

### Project Structure
<pre> Skin-Cancer-Detection/ ├── app.py # Main Flask app ├── wsgi.py # WSGI entry point for deployment ├── skin_cancer_detection.py # CNN model logic + class mappings ├── model.h5 # Trained CNN model ├── requirements.txt # Python dependencies ├── templates/ │ ├── home.html # Upload image page │ ├── results.html # Prediction result page │ └── index.html # Risk prediction form └── README.md # Project documentation </pre>

### Variables Used

Variable Name	Description
pic	Uploaded image file from user
inputimg	PIL image object used for preprocessing
img	NumPy array of shape (1, 28, 28, 3) for prediction
SCD.model	CNN model loaded from model.h5
SCD.classes	List of class labels (AKIEC, BCC, BKL, etc.)
class_ind	Index of predicted class with max probability
result	Final predicted class name
info	Description of the detected skin disease
risk_score	Total score based on user risk input
risk_percentage	Risk percent based on score
risk_level	Risk category: Low / Moderate / High
suggestion	AI-generated advice based on risk level


### Tech Stack
- Python 3.x
- Flask
- Keras / TensorFlow
- NumPy
- PIL (Image Processing)
- HTML / Jinja2 Templates
- JavaScript (for risk module interaction)

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
