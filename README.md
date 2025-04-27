# Screening-Assignment-for-PROSPECT
Modelling:

Thank you for the opportunity.
To model the provided scanned handwritten prescription images, I used the Termux application along with the EasyOCR module.

To start, I first unzipped the 129 prescription images and organized them into a single folder at Storage/Pictures/Prescription. Then, using Python, I began converting all the .jpg files into .txt files.

For convert .jpg images to .txt format we need some libraries for smooth running so for python "pip" is package Installer by using this we download some libraries with below code,

1.pip install easyocr
2.pip install torch torchvision torchaudio
3.pip install opencv-python-headless

These are the libraries required for our modeling. Now, we will create a Python file for the script. To save the file, we use nano, which is a simple text editor in the terminal. When you run the command "nano convert.py" in Termux, it opens the text editor, allowing you to paste and edit your Python code directly.

4.nano convert.py

A blank page will open. In this blank space, we write your Python code to convert .jpg files into .txt files. 

After writing the code,we save the script and run it using the command: python convert.py.

Then, the script will open each .jpg image inside /storage/pictures/prescription/ & It will create .txt files with the recognized text.

Now, all .jpg file are converted into .txt files but all the text appears is mixed, so now we clean up the extracted text to make it more structured by removing extra space, unwanted charecters & organise the text into sections like Patient name, Doctor name, date, medicine etc.

After that we convert all .txt files to .csv file. The purpose of converting a TXT file to CSV is to structure the data into a more organized and tabular format that is easier to analyze, manipulate, and use in various applications.

now again we use command "nano convert_txt_to_csv.py" to save python script for converting.txt to .csv 






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
