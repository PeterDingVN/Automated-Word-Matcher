# Automated-Vietnamese-Phrase-Detecter
Did this phrase exists in this pdf?
Hmmm, how bout their synonyms?
OHHH, 100 files? How can I check all of them for the existence of my wanted words and phrases?
...

## If these are ever your questions, here I have a solution for you!!
Automated-word-matcher can fully automate the process of reading pdf files, finding phrases and words before answering you whether a word/phrase does exist in a given pdf file.

## How to use it?
Note: This code only runs on Jupyternotebook. The reason is some pdf blocks access of google colab, making it necessary to download the file. By running code in Jupyternotebook, you do not have to upload the pdf again to google colab

### Setup
- pip install: PyMuPDF, transformers==4.50.3, torch==2.6.0, pytesseract, pdf2image, opencv-python
- Download packages manually from github before importing:
  + vws: https://github.com/Sudo-VP/Vietnamese-Word-Segmentation-Python
    - click code -> download zip
    - after unzipping, take out folder vws
    - navigate anaconda3 -> Lib -> site-packages
    - drop vws folder into this site-packages
      
  + tesseract: https://github.com/UB-Mannheim/tesseract/wiki
    ![image](https://github.com/user-attachments/assets/5915b1db-2ddb-4980-ba87-c842f76e074a)
    - this will download as .exe file, please run it
      
    - then this appear
      ![image](https://github.com/user-attachments/assets/4a4f04b5-916b-4a39-90c3-eaa179b9e472)
      click ok
    
    - then comes some setup steps which are not important to the functionality of this code, so you can choose whatever and click next
      
    - then this appears
    ![image](https://github.com/user-attachments/assets/2939c579-6863-46c8-b664-c7cd928df638)
    Please choose:
        - "Vietnamses script" for "Additional script data (download)"
        - "Vietnamses" for "Additional langauge data"
          
    - Choose the default path of Tesseract-OCR
      ![image](https://github.com/user-attachments/assets/43547c56-3b0d-4705-b20b-583dd10d0f15)
      Or you can change the code below to the path that you want your Tesseract-OCR to be in (making sure the Tesseract-OCR file stay in the same location as dictated in the below code)
      ![image](https://github.com/user-attachments/assets/1b2f165f-90cd-4d96-94ec-eff920cd4f85)

    - Now click install (the folder Tesseract-OCR will be placed at location you dictated)
![image](https://github.com/user-attachments/assets/b1389c65-4eea-460a-94a4-972b5b855544)

                 
### Usage
- Prepare a folder locally packed with pdf files in need of scanning
![image](https://github.com/user-attachments/assets/a5209fe2-42c4-4091-a358-ae83a1db3524)

- An excel file full of words that you want to extact from the pdf files
![image](https://github.com/user-attachments/assets/c695934c-0bf7-4a32-abfc-c278eab8f2e5)
Note: you have to put all phrases and words only in column A1 (that means maximum 1048576 words) for the code to run properly

- Change the path to pdf folder and excel file accordingly to your own files' name
![image](https://github.com/user-attachments/assets/84820fe0-9e84-4468-b7ae-9c69eaa5b65d)
The output path name is arbitrary, and it will appear on "Home" tab of Jupyternotebook once the code finishes

- Change similarity score to match your desire, with higher score means stricter demand for a phrase/word to be seen as synonymous
![image](https://github.com/user-attachments/assets/260cc46c-cdf7-4d0d-8ed9-d9714e1cf0d2)
![image](https://github.com/user-attachments/assets/32e86cdd-98a1-46f4-aef2-e3120ecf0f82)

- Now run the code and wait for your result!!


# DISCLAIMER:
- this is open-source code and you do not have to obtain my permission for use
- the code, however, contain code from other sources too (links of them will be pasted below), so please consult their policy too when using my code for purposes other than non-profit or educational
- i will not be legally responsible for any misuse of this code

# Reference
I'm very grateful of the people posting materials freely to help me finish this code and my science project, which require reading many pdf files to detect the existence of specific phrases:
- Sudo-VP for https://github.com/Sudo-VP/Vietnamese-Word-Segmentation-Python
- UB-Mannheim for https://github.com/UB-Mannheim/tesseract/wiki
- VinAIResearch for their phoBERT model https://github.com/VinAIResearch/PhoBERT



