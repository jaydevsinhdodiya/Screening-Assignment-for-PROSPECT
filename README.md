# Screening-Assignment-for-PROSPECT

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

The outcome of this project is a single consolidated .csv file, which contains the structured data extracted from all 129 .txt files. This CSV file provides a well-organized and tabular format, making it easier to analyze and manipulate the data for further use. The final .csv file has been attached to this repository for easy access and review.


Limitation:

I used my mobile device for this modeling project, which was not as efficient as working on a laptop. Due to the lack of necessary equipment, I was unable to use multimodal LLMs, which are more accurate for this type of task. Despite these limitations, I did my best with the available resources.

Another challenge was that the scanned images were not always very clear, and the handwriting was not consistently legible. As a result, the OCR model did not always produce accurate text. Additionally, the images varied in terms of section categories, further complicating the process. Some images had unclear or distorted text, making it difficult for the OCR model to recognize certain characters, which impacted the quality of the extracted data.

Furthermore, the inconsistency in formatting and layout across the 129 images posed another obstacle. Not all prescriptions followed the same structure, so organizing the extracted text into a coherent and structured format was challenging. Some sections, such as patient information, medication names, or doctor details, were often mixed or misinterpreted.

While these challenges affected the accuracy of the final results, the outcome is still useful. Despite these limitations, the data extracted provides valuable insights and can be further refined with manual corrections or improved OCR models in the future.



