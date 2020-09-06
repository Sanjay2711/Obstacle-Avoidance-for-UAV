#Obstacle Avoidance for Unmanned Aerial Vehicle using Image Processing

#Problem Statement:
The objective of the project is to develop an algorithm that will make the drone avoid
obstacles autonomously. The drone takes off and flies in a pre-defined trajectory where it must
reach certain destinations. But it must consider the environment given to it i.e.
avoid collisions with objects and crashes.

#Workflow :
set segmentation colors.
calculate the disparity image.
calculate the depth planner image.
calculate the depth perspective image.
calculate the depth vis image.
calculate the segmentation image.
Apply Image Processing Algorithm.
Apply Guidance Algorithm.

#Image Processing :
Every second the algorithm takes a frame/image from the camera on the drone
from several necessary channels:
■ Depth planner image
■ Depth vis image
■ Segmentation image
The algorithm uses the segmentation image along with the depth vis image to
display in binary image objects that are up to a certain meters away from the
drone.
At this point the objects in the image are identified, so we decided to use the
Canny Edges Detection algorithm to find and delineate the object edges in the
image obtained in the previous step first.
A kernel(11x11) is used together with the Erods Algorithm that helps to thicken
pixels with binary values.
Padding(border) to the edges of the image.
Contours Detection Algorithm along with the Red Box Finding Algorithm.
Then each box treated as an object and calculated for each box the distance
from the drone using the depth images. With the help of these calculations by the
algorithm the object that has great potential to collide with the drone.
