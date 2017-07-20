
**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


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

My pipeline consisted of 6 steps. First, I masked the yellow and white colors in the image, and weighted the result with the original image. Then, I converted the images to grayscale. With this 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
