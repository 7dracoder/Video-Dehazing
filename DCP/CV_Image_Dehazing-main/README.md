# CV_Image_Dehazing
Image dehazing using Steering Kernel weighted guided image filtering.

I have implemented the research paper Weighted Guided Image Filtering with Steering Kernel (attached in the folder) and merged it with 3 other research papers, namely Guided Image Filtering, Kernel Regression and Single Haze Removal for the purpose of application in Image Dehazing and Enhancement using SKWGIF.
I have divided the project into three parts namely:

1. Steering Kernel WGIF Implementation
  I have implemented WGIF with a Steering Kernel (SKWGIF). GIF and WGIF suffers from Halo Artifacts. SKWGIF takes advantage of WGIF over GIF while leveraging the edge direction     more sufficiently. The code uses Steering Kernel which in turn requires local gradient matrices. The steering kernel helps us to identify the energy dominant directions. I have   used different values for the radius of the local window and the regularization parameter. The comparison results clearly show the advantage of using SKWGIF over WGIF and GIF.

2. Image Dehazing Using SKWGIF and Histogram Equalization
  I have implemented Image Dehazing for Grayscale Images. First, I applied Histogram Equalization to increase the dynamic range of the image. Then I have used SKWGIF for detail   enhancement and edge retention which reduces the contrast of background noise. The Code uses Histogram Equalization function followed by SKWGIF function. The results are           presented by varying the values for radius of local window and regularization parameter. SKWGIF gives better results than GIF and WGIF due to supreme edge detection.
 
3. Coloured Image Dehazing Using SKWGIF
 I have implemented image dehazing for coloured images using SKWGIF and Dark Channel Prior. Instead of using Laplacian matrix to refine the haze transmission map, I simply
 use WGIF to filter the raw transmission map under the guidance of the hazy image. The code uses Dark Channel Function, AtmLight Function, Transmission Refine and Recovery         function along with SKWGIF function for guided image filtering. The results come out with a large amount of haze removed and visually similar to the original method while being a  simpler algorithm and less overhead.
