
[//]: # (Image References)

[image1]: /test_images_output2/1masked.jpg "Mask - Yellow and White"
[image2]: /test_images_output2/2gray.jpg "Grayscale"
[image3]: /test_images_output2/3blurgray.jpg "Blurred Grayscale"
[image4]: /test_images_output2/4edges.jpg "Edges"
[image5]: /test_images_output2/5edgeswithmaskedregion.jpg "Masked Region"
[image6]: /test_images_output2/6final.jpg "Result"

---

### Reflection

### 1. Basic pipeline


My pipeline consisted of 10 steps: 


**1- Mask the yellow and white colors in the image, and weight the result with the original image.**

![alt text][image1]


**2- Convert the result image to grayscale.**

![alt text][image2]


**3- Blur.**

![alt text][image3]


**4- Use Canny Edge Detection.**

![alt text][image4]


**5- Mask the Region of Interest**

![alt text][image5]

**6- Use the Hough Transform to find lines from Canny Edges**

**7- Separate lines with positive and negative slopes.**

**8- Find two linear interpolations, one for positive slopes and one for negative slopes.**

**9- Use a simple low-pass filter to filter out the high frequency noise (only video).**

**10- The result:**

![alt text][image6]




In order to draw a single line on the left and right lanes, I modified the draw_lines() function by separating lines with positive and negative slopes. Then, I could make two linear interpolations, one for positive slopes and one for negative slopes (left and right lanes, respectively).




### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the car makes abrupt turns. The low-pass filter can create a significant delay on the algorithm.

Another shortcoming would be what would happen when the car is driving in roads that has different line colors. This algorithm may not work properly, since it only "highlights" white and yellow lines.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to find other ways to mask the lines on the street.

Another potential improvement could be to find another way to filter out the high frequency noise.
