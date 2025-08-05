# Lemon vs Melon Image Classifier

A Flask web application that classifies images as either lemons or melons using a pre-trained machine learning model.

## Features

- 🍋🍈 Image classification for lemons and melons
- Modern, responsive web interface
- Drag and drop file upload
- Real-time image processing
- Beautiful UI with gradient backgrounds

## Setup Instructions

### 1. Install Dependencies

First, make sure you're in your virtual environment, then install the required packages:

```bash
pip install -r requirements.txt
```

### 2. Verify Model File

Ensure your trained model file `image_classifier.pkl` is located at:
```
C:\Users\santhosh\Desktop\Machine Learning\Poly_tech_aug_2025\image_classifier.pkl
```

### 3. Run the Application

Start the Flask development server:

```bash
python app.py
```

The application will be available at: `http://localhost:5000`

## Usage

1. Open your web browser and navigate to `http://localhost:5000`
2. Click on the upload area or drag and drop an image file
3. Select an image file (JPG, PNG, etc.)
4. Click "Classify Image" to get the prediction
5. View the result and try another image

## File Structure

```
Poly_tech_aug_2025/
├── app.py                 # Main Flask application
├── image_classifier.pkl   # Trained model file
├── requirements.txt       # Python dependencies
├── README.md            # This file
└── templates/
    ├── index.html       # Upload page
    └── result.html      # Results page
```

## Model Information

The application uses a pre-trained machine learning model that:
- Extracts RGB mean values from images using OpenCV
- Uses Support Vector Machine (SVC) classifier
- Expects 3 features (R, G, B mean values)
- Classifies images as either lemon (0) or melon (1)

## Troubleshooting

- **Model not found**: Ensure `image_classifier.pkl` exists in the specified path
- **Import errors**: Make sure all dependencies are installed with `pip install -r requirements.txt`
- **Port already in use**: Change the port in `app.py` or stop other applications using port 5000

## Customization

To modify the image preprocessing:
- Edit the `preprocess_image()` function in `app.py`
- Adjust the image size, normalization, or other preprocessing steps as needed for your model

## Technologies Used

- **Flask**: Web framework
- **OpenCV**: Image processing and feature extraction
- **Pillow (PIL)**: Image handling
- **NumPy**: Numerical computations
- **scikit-learn**: Machine learning model loading
- **HTML/CSS/JavaScript**: Frontend interface 