# ID Card Details Extraction Pipeline
## Overview
This project is an end-to-end pipeline for extracting textual details from images of ID cards placed on arbitrary surfaces. The pipeline integrates multiple tasks, including image classification, segmentation, de-skewing, text segmentation, and OCR (Optical Character Recognition).

The pipeline is developed using deep learning (DL), convolutional neural networks (CNN), and traditional image processing techniques. Each step is modular, allowing for seamless integration and extensibility.
## Features
### ID Card Detection:

    Developed a classification network using deep learning and CNN to identify images containing ID cards.

### ID Card Segmentation:

    Extracted the ID card region from detected images using a U-Net segmentation network.

    Divided the image into foreground (ID card) and background regions.

### ID Card De-Skewing:

    Corrected skewed ID card images using Hough Transform and SIFT (Scale-Invariant Feature Transform) techniques.

### Text Segmentation:

     Segmented the text-containing portions of the de-skewed ID card as foreground while retaining the remaining areas as background.

### Text Recognition:

     Applied OCR (Optical Character Recognition) to read text details from the segmented ID card image.

### End-to-End Pipeline:

     Built a complete pipeline integrating all the above steps to process an image of an ID card and output its textual details.

## Project Architecture
The pipeline comprises six distinct tasks:

### Classification Network: 
Detects whether an image contains an ID card.

Tools/Technologies: Deep Learning (DL), Convolutional Neural Networks (CNN).

### ID Card Segmentation: 
Segments the ID card region from the background.

Tools/Technologies: U-Net, Python, Sklearn.

### De-Skewing ID Card: 
Corrects perspective distortions of the ID card.

Tools/Technologies: Hough Transform, SIFT (Image Processing Techniques).

### Text Segmentation: 
Identifies and extracts text portions of the ID card.

Tools/Technologies: Deep learning, python, numpy, matplotlib, pandas.

### OCR for Text Extraction: 
Reads textual information from the ID card.

Tools/Technologies: Optical Character Recognition (OCR).

### End-to-End Integration: 
Combines all steps into a single streamlined proce.

## Installation
Follow the steps below to set up the project:

Clone the Repository:
```git clone https://github.com/your-username/id-card-details-extraction.git
cd id-card-details-extraction```

Install Dependencies:
Ensure you have Python 3.8 or above installed. Install required dependencies:
```pip install -r requirements.txt```

Prepare Data:

Place your dataset in the data folder, ensuring it has subfolders for training and testing images as required.

Run the Pipeline:
To process an image of an ID card:
```python pipeline.py --input path/to/your/image.jpg```

## Usage
The pipeline takes an input image containing an ID card placed on a random surface and outputs the textual details from the ID card.

## Example command
```python pipeline.py --input ./test_images/sample_id.jpg```

## Expected Output:
Textual details extracted from the ID card, such as name, ID number, and date of birth.

## Dependencies

Python (>=3.8)

TensorFlow / PyTorch (for DL models)

OpenCV (for image processing)

Tesseract-OCR (for text recognition)

Additional libraries: numpy, sklearn, matplotlib
