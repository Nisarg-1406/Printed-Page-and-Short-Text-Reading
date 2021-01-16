# Printed-Page-and-Short-Text-Reading

## Table of Contents - 
* [About Project](#about-project)
* [Detailed Explanation about Project](#detailed-explanation-about-project)
* [Output Images](#output-images)
* [About Me](#about-me)

## About Project
* This project is the computer vision part which is aiming for reading the printed pages and the short text using Tesseract OCR. It takes an input image and with the use of the algorithm it convert the image into text. It gives the correct output on the printed pages as well as on the short Printed Text.

## Detailed Explanation about Project
1. It is using the Tesseract OCR library. Tesseract is an OCR engine with support for unicode and the ability to recognize more than 100 languages out of the box. It can be trained to recognize other languages. Tesseract is finding templates in pixels, letters, words and sentences. It uses two-step approach that calls adaptive recognition. It requires one data stage for character recognition, then the second stage to fulfil any letters, it wasn’t earlier Processed. This can be achieved by - `!sudo apt install tesseract-ocr`. 

2. Then to install the **pytesseract** using `!pip install pytesseract` - The version number is : **pytesseract - 0.3.7**. Python-tesseract is an optical character recognition (OCR) tool for python. That is, it will recognize and “read” the text embedded in images. Python-tesseract is a wrapper for Google’s Tesseract-OCR Engine. It can read all image types supported by the **Pillow and Leptonica imaging** libraries, including **jpeg, png, gif, bmp, tiff, and others**. Additionally, if used as a script, Python-tesseract will print the recognized text instead of writing it to a file.

3. About Importing the necessary Libraries - 
  * `import pytesseract` - After installing we would be importing the `pytesseract`.
  * `import shutil` - Shutil module in Python provides many functions of high-level operations on files and collections of files. The standard utility modules helps in automating process of copying and removal of files and directories. If we do `shutil.copyfile(source, destination)` then we copy the content from source to destination.
  * `import os` - It is used for creating the directories.
  * Then we would be using `PIL` - Pillow is a Python Imaging Library (PIL), which adds support for opening, manipulating, and saving images and `from PIL import Image` will loads the image and read the image.
    ```
    import pytesseract
    import shutil
    import os
    try:
        from PIL import Image
    except ImportError:
        import Image
    ```
 
4. Finally we would be importing and uploading the files by using - 
    ```
    from google.colab import files
    uploaded = files.upload()
    ```
 
5. And in the last step we would be opening the image and would be converting it into the string (Text) and would be storing it into variable named `extractedInformation` and finally would be printing out the result. 
    ```
    extractedInformation = pytesseract.image_to_string(Image.open('FILE_NAME.jpg'))
    print(extractedInformation)
    ```

## Output Images

  <img src = "Images/Printed Pages - Input Image 1.jpg" width = "600">
  <img src = "Images/Printed Pages - Output Image 1.jpg" width = "600">
  <img src = "Images/Short Text - Input Image 2.jpg" width = "200"> 
  <img src = "Images/Short Text - Output Image 2.jpg" width = "200">

## About Me
**IF YOU LIKED MY WORK, PLEASE HIT THE STAR BUTTON, AND IF POSSIBLE DO PLEASE SHARE, SO THAT COMMUNITY CAN GET BENIFIT OUT OF IT BEACUSE I AM EXLPANING EACH AND EVERY LINE OF CODE FOR EACH AND EVERY PROJECT OF MINE.**

Also I am Solving **Algorithms and Data Structure Problems from more than 230 Days Without any off-Day and have solved more than 405 Questions on various topics and posting my solutions on Github Daily**. You can Visit my Profile of LeetCode here - **https://leetcode.com/Nisarg1406/**

I am good at Algorithms and Data structure and I have good Projects in Machine learning and Deep Learning (Computer Vision). **I am and would be posting the detialed explantion of each and every project working**. I am activily looking for an Internhip in **Software development enginering (SDE) Domain and Machine learning Domain**.

You can contact me on my mail ID - nisarg.mehta18@vit.edu OR nisargmehta2000@gmail.com and even Contact me on LinkedIn - https://www.linkedin.com/in/nisarg-mehta-4a378a185/
