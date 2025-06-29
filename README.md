##Liver Tumor Detection using U-Net (Django Based)
This project is a web application built using Django that allows users to upload liver CT scan images and automatically detects tumor regions using a trained U-Net deep learning model. The application displays the original uploaded image alongside the predicted tumor region and also generates a downloadable PDF report.

#Features
Upload liver CT scan images (PNG, JPG format)

Automatic tumor detection using a pre-trained U-Net model

Visual overlay of predicted tumor region on original image

PDF report generation including patient name and diagnosis result

Clean and responsive web interface

Technologies Used
Python

Django

TensorFlow / Keras (U-Net Model)

OpenCV

ReportLab (PDF generation)

HTML/CSS (Frontend templates)

#Project Structure

liver_tumor_project/
├── liver_app/
│   ├── templates/
│   │   ├── upload.html
│   │   └── result.html
│   ├── static/
│   │   └── outputs/
│   ├── unet_model/
│   │   └── predict.py
│   ├── utils.py
│   └── views.py
├── media/
│   └── uploaded images and predicted results
├── model.h5  # Trained U-Net model
└── manage.py
#How to Run
Clone the Repository
git clone https://github.com/yourusername/liver-tumor-detection.git
cd liver-tumor-detection
Install Dependencies

pip install -r requirements.txt
Add the trained model

Place your model.h5 file in the root folder or as required in your predict.py path.

#Run Migrations
python manage.py makemigrations
python manage.py migrate
Run Server

python manage.py runserver
Visit in browser
http://127.0.0.1:8000/
##Notes
Ensure you are using grayscale images as input or modify the model to accept RGB.

The media/ folder is used for saving uploaded and predicted images.

PDF reports are saved inside media/outputs/ and can be viewed directly via the browser.

#License
This project is for educational and research purposes only.
