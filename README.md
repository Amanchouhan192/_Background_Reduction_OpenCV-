# :heart_eyes:_Background_Reduction_OpenCV-
In this small project the deduction of the background from the the video/image.. ; )

# :stuck_out_tongue_winking_eye:Small_Source_code
```py
import numpy as np
import cv2
# for apply the video effect and '0' for the Camera 1(webcam)
cap = cv2.VideoCapture(0)
# createBackgroundSubtractorMOG2() this function for the Background
#Subtractor
fgbg = cv2.createBackgroundSubtractorMOG2()

while(1):
    ret, frame = cap.read()

    fgmask = fgbg.apply(frame)
 
    cv2.imshow('fgmask',frame)
    cv2.imshow('frame',fgmask)

    
    k = cv2.waitKey(30) & 0xff
    if k == 27:
        break
    

cap.release()
cv2.destroyAllWindows()
```
# :fire: Output
<img src='https://i.imgur.com/o1sPi5M.png' />


# :notebook:Note
```before run the above code ,you should  install the the all dependencies/files.```


