# Seam_Carving_Multiop

Seam Carving and multioperators Implementation  
by Preeti Saharan and Shifa Samreen.

Code was tested in Matlab 2016a.

To run GUI, run sc_gui.m in Matlab.

Best place to start would be to look at the sc_gui.m file and trace through to the other functions. A word of
warning, the code is very messy at times and little documented.

The GUI was implemented in Matlab. The following are the features:

1- Resize
Will resize the media to target size. Resizing is done on the original image and not on
the current shown image.

2- Simple Reduction
If enabled, program uses simple reduction technique which removes horizontal seams, then vertical
seams. If disabled, the uses optimal seam ordering technique which takes longer. This is enabled
by default in the case of video.

3- Forward Energy
If enabled, program computes optimal seams using Forward energy (results are better). If disabled,
program uses the default backward energy.

4- Graph Cut Approach
If enabled, program uses graph cut metho to find the optimal seam. If disabled, the default is the
use of dynamic programming approach. This is enabled by default in the case of video.

5- Show Seams
Shows the optimal seams on the image. This is only enabled for images.

6- Remove Object
Allows user to apply a mask on the image for removal. Only works for images. To apply the mask, hold
the left mouse button down and drag your mouse to cover the region you'd like removed.

7- Amplify
Amplifies the original content in the image by scaling it up by 120% then applying seam carving to reduce
back to original size.

8-Show Horizontal/Vertical Seam Cut
Shows the resulting graph cuts that are computed when using the graph cut approach. In the case of video,
it shows the 3D seam manifold.

9- Applying Protection Mask
In the case of images, the user is able to apply a protection mask, hold the right mouse button down and 
drag your mouse to cover the region you'd like protected

10- Line Detection
Detects the lines and edges in the image and perform the reduction and enlargement in such a way that
the lines and edges in the image don't get distoted.

11- Gaussian
A new framework to speed up seam carving using Gaussian pyramid concept. It reduces the computational
time to approximately one-fourth of the time consumed by simple reduction and enlargement using backward energy. 
