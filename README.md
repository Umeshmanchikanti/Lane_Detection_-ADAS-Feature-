# Lane_Detection_-ADAS-Feature-
What is Lane Line Detection?
Lane Detection is a computer vision task that involves identifying the boundaries of driving lanes in a video or image of a road scene.
Introduction & Abstract
A vehicle that can sense its surroundings and function without human assistance is called an autonomous car. The presence of a human passenger in the car is not mandatory, nor is it necessary for a human passenger to take control of the vehicle at any point. All the functions of a skilled human driver can be performed by an autonomous vehicle, which can travel anywhere a conventional car can. Identifying lanes and maintaining lane separation is the fundamental need for self-driving cars.
The driver support systems found in modern cars are essential to driver safety and accident prevention. Roads are difficult to see. The road-vehicle distance is estimated. An on-board camera windscreen-viewing vision system is presented in this study. A car camera records the front view and can detect lanes using a variety of techniques. Lane boundaries are determined using the Hough transform on two fitted plots. The proposed lane detection technique is applicable to both painted and unpainted straight and curved roadways under different weather conditions. There is no need for lane offset, crossing time, or breadth using the suggested solution. Calibration of the camera is not required. The system was evaluated in a variety of shadow, illumination, and speed limit-free road conditions. Road lanes are reliably detected by the gadget. 
Brief steps involved in Road Lane Detection
Road Lane Detection necessitates identifying autonomous vehicles' paths and preventing them from accidentally changing into other lanes. By examining the visual input, lane recognition algorithms are able to accurately determine the position and boundaries of the lanes. Both autonomous vehicle systems and advanced driver assistance systems (ADAS) mostly depend on them. We are going to discuss one of these lane detection methods today. The actions to be taken are:

 
Flow of Execution:
 
Capturing and decoding video file: Using the VideoFileClip object, we will record the video. Once the recording has been started, each video frame is decoded, or turned into a series of images.
Grayscale conversion of image: Since processing a single channel image is quicker than processing a three-channel colorful image, the RGB format of the video frames is transformed to Grayscale.
Reduce noise: It is essential to do image smoothing before proceeding, as noise might produce misleading edges. This is accomplished using Gaussian blur. A common method of picture filtering that reduces noise and improves image qualities is Gaussian blur. A weighted average that takes into account the pixels around each pixel is applied to each one, and the weights are chosen using a Gaussian distribution. This blurring technique produces softer, more aesthetically pleasing images by eliminating high-frequency features and enhancing overall image quality.
Canny Edge Detector: It traces the edges with significant intensity variations and computes the gradient in every direction of our blurry image.
Region of Interest: Only the area covered by the road lane will be considered in this stage. This is where a mask the same size as our road image is made. And every pixel in our clever image and this mask is subjected to a bitwise AND operation. In the end it conceals the clever picture and displays the area of interest indicated by the mask's polygonal outline.
Hough Line Transform: The Hough transformation is an image processing feature extraction technique that locates simple geometric features like circles and lines. It is feasible to recognize shapes by accumulating voting points by turning the picture space into a parameter space. The probabilistic Hough Line Transform will be employed in our algorithm. With the probabilistic Hough transformation, the Hough transformation has been expanded to handle computational complexity. To expedite processing while maintaining shape detection accuracy, it selects a subset of picture points at random and applies the Hough transformation just to those points.
Draw lines on the Image Frame: We apply lane lines to our visual input image by overlaying them after utilizing the Hough Line Transform to detect them in our field of interest. 
