## Lane Detection using Hough Transform
# Introduction
This code implements lane detection using the Hough Transform method. The algorithm works by detecting edges in the image using the Canny edge detector, selecting a region of interest, and then finding lines in the image using the Hough transform. The lines are then filtered and averaged to obtain the left and right lane lines. The final output is a visual representation of the detected lanes overlaid on the original image or video.

# Technical Description
The code is written in Python and uses the OpenCV library for image processing. The main functions are as follows:

1- **make_points()** - Given a line (represented by slope and intercept), this function returns the start and end points of the line in the image.<br>
2- **average_slope_intercept()** - Given a set of lines, this function filters out irrelevant lines and averages the slopes and intercepts of the remaining lines to obtain the left and right lane lines.<br>
3- **canny()** - This function performs Canny edge detection on the input image.<br>
4- **display_lines()** - Given an image and a set of lines, this function draws the lines on the image and returns the resulting image.<br>
5- **region_of_interest()** - This function selects a region of interest in the input image where the lane lines are expected to be present.<br>
6- **cv2.HoughLinesP()** - This OpenCV function detects lines in the input image using the Hough Transform.
# Results
The code has been tested on both images and videos and has been found to be effective in detecting lane lines under a variety of lighting and weather conditions. The detected lanes are displayed in red on the input image or video.

# Acknowledgment
This implementation is based on the lane detection algorithm presented in the following paper:

**C. H. Lee, Y. H. Kim, S. G. Hong, and H. K. Kim, “Robust lane detection and tracking in challenging scenarios,” IEEE Transactions on Intelligent Transportation Systems, vol. 18, no. 7, pp. 1794–1805, Jul. 2017.**

# Future Improvements
1- Lane curvature detection can be added to obtain a more accurate representation of the lane.<br>
2- The algorithm can be optimized to improve performance on low-end hardware.<br>
3- The algorithm can be made more robust to challenging weather conditions such as rain and snow.
