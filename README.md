# Screening-Assignment-for-PROSPECT
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
