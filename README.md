# The Birthday Problem Simulation

<p align="center">
  <img src="https://github.com/niravpansuriya/the_birthday_problem_simulation/blob/master/birthday_paradox_cover_cropped.jpg" title="Cover">
</p>

- This is the simulation of **The Birthday Problem**.
- If you don't know what is the birthday problem, this please refer my this detailed [article](https://medium.com/@pniravc36/the-birthday-problem-cd61258fcb02?source=friends_link&sk=f11355641cbc6b06b70f11cee3026e53) on medium.

### How it works?




<p align="center">
  <img src="https://github.com/niravpansuriya/smart-video--recording-with--gesture-detection/blob/master/defects.JPG" title="Defects">
</p>

- My basic task here to detect whether there exist three fingures in the frame.
- It start capturing video frame by frame.
- For each frame, this program do some processing on image, for detect 3 fingures.
  - Crop the frame in rectangle shape.
  - Convert RGB image to gray scale.
  - Apply gaussian blurred low pass filter on image to remove noise.
  - Find contours. Contours are the curves joining all the continuous points. 
  - Find largest contour. Most probably it will be the palm, if there exist palm in a frame.
  - Find hull in palm. Hull in plam is space between two fingures
  - Now I have hull. Any deviation of the object from this hull can be considered as convexity defect.
  - With the help of defects, I find the Convex Points and with these points, I find angle of hull.
  - If angle is less than 90, then it is the hull between two findures.
  - And number of such Hulls + 1 is the number of fingures.
  - If number of fingers is three, then this program starts recording.



### Prerequisites

- [Python 3.0 +](https://www.python.org/downloads/) on 
- [OpenCV](https://opencv.org/) - Library, aimed for real-time Computer Vision.


## Authors

* **Nirav C. Pansuriya** 
