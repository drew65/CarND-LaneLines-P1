# CarND-LaneLines-P1
This is the first project of the Udacity Self Driving Car Nano Degree, second cohort, Nov 2016.
It uses OpenCV in Python to detect lane lines on the road via video from a dashboard camera.  The detected lane lines are, once detected, highlighted in red.  It is written in a Jupyter notebook.

It uses the following pipeline on each fame from the video feed that:
1) Extracts the colour yellow into s separate image.
2) Converts the original and yellow image to gray.
3) Merges the two gray images.
4) Smooths the image with a Gaussian  blur.
5) Defines an area of interest on the image.
6) Runs canny edge to extract edges.
7) Runs Hough transform on masked image. to extract lines
8) Removes lines tending towards the horizontal.
9) Separates the lines into left and right buckets and defines best fit line coordinates for each side.
10) Merges the lane lines with those from the previous frame if they exist, to reduce jitter.
11) Merges the resulting lane lines with the original and returns the result.
