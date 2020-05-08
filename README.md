# Computer_Vision-Road-LANE-detection-
detect road lane using python computer vision

Lane Detection Pipeline:
Convert original image to grayscale.
Darkened the grayscale image (this help in reducing contrast from discoloured regions of road)
Convert original image to HLS colour space.
Isolate yellow from HLS to get yellow mask. ( for yellow lane markings)
Isolate white from HLS to get white mask. (for white lane markings)
Bit-wise OR yellow and white masks to get common mask.
Bit-wise AND mask with darkened image .
Apply slight Gaussian Blur.
Apply canny Edge Detector (adjust the thresholds — trial and error) to get edges.
Define Region of Interest. This helps in weeding out unwanted edges detected by canny edge detector.
Retrieve Hough lines.
Consolidate and extrapolate the Hough lines and draw them on original image.
