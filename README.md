# esp8266-ADNS3080-Supertrack
Goal is to build a high speed, low latency, 2D or 3D tracking system for low weight robotic systems.

Based on the ESP8266 as the computing core and ADNS3080 for high speed image capture.

Idea is to use similar techniques an algorithms as been used in the laser distance project.

--------------------------------

#problem
Getting clear results from camera captured objects. 
For example tracking a light is a heavier task then expected. 

Tracking a light spot (LED E.g.) in an image is only a feeble and not reliable result especially in high speed applications.


#solution
By switching the light in a (by the camera) known pattern, you can make much more exact predictions about the position of the light.

#example:

Time-------------------------------------------------------------------------->

module: 
-------------------------------------------------------------------------
Camera  |take image  | -> | take image | -> | take image ...
Light   |light off   | -> | light on   | -> | light off ...
CPU     |         save image1        save image2        
                                             |
                                             |---> by calculating the difference of the light intensity of image1 and image2
                                             in every pixel you can calculate a 'hot spot' this spot is exactly where the 
                                             light source is.



... by the way. watch this graph in 'raw'
