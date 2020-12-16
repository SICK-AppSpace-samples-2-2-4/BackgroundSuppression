## BackgroundSuppression
Providing a scan view which shows the detected foreground points in front of a 
teached-in background contour.
### Description
After startup the scan view shows the original scan points retrieved from file.
After 75 scans the measured scan points define the background contour. Afterwards the app 
enters the detection phase and every scan is filtered in the following way:
  
1. The measured scan points are subtracted from the background. 
2. If the difference is larger than 150 mm the scan point is regarded as foreground point and 
   the distance remains unchanged. 
3. If the distance is less than 150 mm the scan point is regarded as background point and the
   distance is set to zero

### Topics
Algorithm, Scan, Sample, SICK-AppSpace