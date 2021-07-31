# Face_detection

This project is done using Pycharm IDE and Python, it is a Face recognition using OpenCV while performing object detection using Haar feature-based cascade classifiers for detecting face.

# First Step :
Import and initialize\
Start by importing OpenCV and create a directory (ex: Cascades) to gather all Haar classifiers files that you want to use in you project, then use their path to load them into your project.

Note: you can find Haar cascade classifiers files here (https://github.com/opencv/opencv/tree/master/data/haarcascades)

import cv2\
face_casecade = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')

# Second Step:
Call the classifier function\
\
img = cv2.imread('elone.jpeg')\
gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)\
faces = face_casecade.detectMultiScale(gray, 1.1, 1)

# Third Step:
Detecting Face\
The function will detect faces on the image. Next, we must "mark" the faces in the image, using, for example, a blue rectangle. If faces are found, it returns the positions of detected faces as a rectangle with the left up corner (x,y) and having "w" as its Width and "h" as its Height ==> (x,y,w,h). This is done with this portion of the code:

for (x, y, w, h) in faces:\
    cv2.rectangle(img, (x, y), (x+w, y+h), (255, 0, 0), 2)\

cv2.imshow('img', img)\
cv2.waitKey()
![WhatsApp Image 2021-07-31 at 11 53 41 PM](https://user-images.githubusercontent.com/86194970/127752283-b9292dce-ea9b-41f2-8022-b5eef9e6ad7e.jpeg)

# The Result
To test the program i used a photo of Elone Mask

![WhatsApp Image 2021-08-01 at 12 04 50 AM](https://user-images.githubusercontent.com/86194970/127752367-892075d5-b61a-4e5f-aef1-4509188da290.jpeg)
