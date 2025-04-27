# Screening-Assignment-for-PROSPECT
Modelling:

Project Overview:

In this project, I modeled the conversion of scanned handwritten prescription images into structured data using the Termux application along with the EasyOCR module. The objective was to process prescription images (.jpg format) and extract meaningful information such as patient details, prescription items, and doctor's information into a structured format for analysis.

Steps Involved:

1. Organizing Prescription Images: I started by unzipping the 129 scanned prescription images and organized them into a single folder located at Storage/Pictures/Prescription.


2. Installing Required Libraries: To facilitate the conversion of images to text, several Python libraries are required. These libraries were installed using pip (Python’s package installer) with the following commands:

pip install easyocr
pip install torch torchvision torchaudio
pip install opencv-python-headless


3. Creating the Python Script for Image to Text Conversion: A Python script was created to process the .jpg files and convert them into .txt files. The script uses EasyOCR to extract text from each image. To save the Python script, I used the nano text editor in Termux, which can be accessed with the following command:

nano convert.py

In the script, I used EasyOCR to read each image from the folder Storage/Pictures/Prescription/ and saved the recognized text in .txt files.


4. Data Cleaning and Structuring: After the text was extracted from the images, I cleaned up the data by removing extra spaces, unwanted characters, and organized the text into sections (e.g., Patient Name, Doctor’s Name, Date, Medicine, etc.) for better readability and analysis.


5. Converting .txt Files to .csv Format: The next step was to convert the cleaned .txt files into a .csv format. This conversion was necessary to organize the data into a structured, tabular format, making it easier to analyze, manipulate, and use in various applications.

For this task, I created another Python script and saved it using the following command:

nano convert_txt_to_csv.py

After writing and saving the script, I ran it using:

python convert_txt_to_csv.py

This script processes all .txt files in the folder and converts them into .csv file.






Evaluation Strategy:

1. Manual Verification:

I manually reviewed the structured data extracted from the prescriptions.
I compared the predicted values (Patient Name, Doctor Name, Date, Medicines, Instructions) with the true information visible in the prescription images.

2. Overall Pipeline Performance:

Overall accuracy was measured by checking how many complete prescriptions (all fields correct) were successfully extracted.

3. Error Analysis:

I analyzed incorrectly extracted examples to understand the common sources of errors, such as:
Poor handwriting OCR misreadings Missing fields due to image qualityBased on the analysis, suggestions for improvements were identified (e.g., image pre-processing, better OCR models).

4. Limitations Noted:

Variations in handwriting styles and low-resolution images significantly impacted extraction accuracy.
Some structured fields like "instructions" were harder to capture due to their free-text nature.

My Extraction Pipeline & Multimodal Model Usage: 

I built a pipeline that uses OCR (Optical Character Recognition) to extract raw text from scanned prescription images.
Then, I applied text cleaning techniques to remove noise and irrelevant characters.
Next, I structured the extracted text into important fields: Patient Name, Doctor Name, Date, Medicines, and Instructions.
Finally, I exported the structured data into a CSV file for easy analysis and further processing.


/prescription_extraction_project
    ├── images/                # All prescription images
    ├── extracted_texts/        # Text files from OCR
    ├── cleaned_texts/          # Cleaned text files
    ├── scripts/
    │    ├── ocr_extraction.py  # OCR extraction script
    │    ├── text_cleaning.py   # Text cleaning script
    │    ├── structured_data.py # Extraction of structured fields
    ├── output.csv              # Final structured data
    ├── README.md               # Project Summary (with above 3 sections)
