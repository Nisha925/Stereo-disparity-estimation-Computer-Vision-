# Stereo-disparity-estimation-Computer-Vision

For the given two images, compute the disparity map. 

A disparity map is nothing but an output-image, which shows how much a pixel has moved from the one view to the other.
For example, if a pixel at location (x,y) has translated by 10 pixels, then the disparity map value at (x,y) will be 10.

Note that unlike in assignment 1, here the scene is not a 2D scene (i.e. the objects are at different depths. Thus, there will not be a global parametric motion between pixels)

To compute the disparity of each pixel, choose a window of some size (e.g. 5 x 5 to 15 x 15), around a pixel in the reference image,
Then  translate a window in the other (test) image and compute the translation value at which both the windows have the closest match.
The 'closest' match is computed based on some distance metric between the pixel value in the reference image window and the test image windows.
For some basic distance metric please see the document "stereo disparity review.pdf" uploaded above

In this particular case, the camera is only translated horizontally. 
Hence you would only have to translate the test window in the horizontal direction.
