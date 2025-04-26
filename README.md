# Screening-Assignment-for-PROSPECT
Modelling:

First, I did not have a laptop so I did this work from my mobile. 
For modelling of given scanned priscription images I used termux & EasyOCR module to do modelling.





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
