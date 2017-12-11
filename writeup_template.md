---

My pipeline consisted of 7 steps. 

First, I converted the images to grayscale, then I apply Gaussian Blur to the gray image, then I apply this blur and gray image to Canny. 

At this point I got a edge of this image, then I define a region of interest for this image, to focus on the very important angle of this image taken by the camera, and then I use this region to mask the image. 

After doing all these steps, I got a group of lines(endpoints), then I apply these lines to a blank image. 

At last I max all these lines to the original image, this will output a Lane-image.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by try to find two lines that has biggest distance on the bottom.

One potential shortcoming would be what would happen when the car try to make a turnning on the road

Another shortcoming could be when sun light is too brighten, the lane line on the road will be very difficult to identify.

A possible improvement would be to imrove the sensitivity of brighten light

Another potential improvement could be to adopt to the car turnning circumstances
