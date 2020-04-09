---
layout: page
title: Quality Metrics
permalink: /6-metrics/
---

This section defines the objective image quality metrics that will be used for the assessment of learning-based image coding solutions.

### MS-SSIM Definition and Computation
Multi-Scale Structural SIMilarity (MS-SSIM) [1] is one of the most well-known image quality evaluation algorithms and computes relative quality scores between the reference and distorted images by comparing details across resolutions, providing high performance for learning-based image codecs [2]. The MS-SSIM [1] is more flexible than single-scale methods such as SSIM by including variations of image resolution and viewing conditions. Also, the MS-SSIM metric introduces an image synthesis-based approach to calibrate the parameters that weight the relative importance between different scales. A high score expresses better image quality.

The source code of this metric can be downloaded [here](https://ece.uwaterloo.ca/~z70wang/research/iwssim/).

### VMAF Definition and Computation
The Video Multimethod Assessment Fusion (VMAF) metric [3] developed by Netflix is focused on artifacts created by compression and rescaling and estimates the quality score by computing scores from several quality assessment algorithms and fusing them with a support vector machine (SVM). Even if this metric is specific for videos, it can also be used to evaluate the quality of single images and has been proved that performs reasonably well for learning-based image codecs [2]. Since the metric takes as input raw images in the YUV color space format, the PNG (RGB color space) images are converted to the YUV 4:4:4 format using FFMPEG (BT.709 primaries). A higher score of this metric indicates better image quality.

The source code of this metric can be downloaded [here](https://github.com/Netflix/vmaf).

###	VIF Definition and Computation
The Visual Information Fidelity (VIF) [4] measures the loss of human perceived information in some degradation process, e.g. image compression. VIF exploits the natural scene statistics to evaluate information fidelity and is related to the Shannon mutual information between the degraded and original pristine image. The VIF metric operates in the wavelet domain and many experiments found that the metric values agree well with the human response, which also occurs for learning-based image codecs. A high score expresses better image quality.

The source code of this metric can be downloaded [here](https://live.ece.utexas.edu/research/Quality/VIF.htm).

###	NLP Definition and Computation
The Normalized Laplacian Pyramid (NLPD) is an image quality metric [5] based on two different aspects associated with the human visual system: local luminance subtraction and local contrast gain control. NLP exploits a Laplacian pyramid decomposition and a local normalization factor. The metric value is computed in the normalized Laplacian domain, this means that the quality of the distorted image relative to its reference is the root mean squared error in some weight-normalized Laplacian domain. A lower score express better image quality.

The source code of this metric can be downloaded [here](http://www.cns.nyu.edu/~lcv/NLPyr/).

### FSIM Definition and Computation
The feature similarity (FSIM) metric [6] is based on the computation of two low level features that play complementary roles in the characterization of the image quality and reflects different aspects of the human visual system: 1) the phase congruency (PC), which is a dimensionless feature that accounts for the importance of the local structure and the image gradient magnitude (GM) feature to account for contrast information. Both color and luminance versions of the FSIM metric will be used. A high metric value express better image quality.

The source code of this metric can be downloaded [here](https://www4.comp.polyu.edu.hk/~cslzhang/IQA/FSIM/FSIM.htm).

### References

[1] Z. Wang, E. P. Simoncelli and A. C. Bovik, “Multi-scale Structural Similarity for Image Quality Assessment”, 37th IEEE Asilomar Conference on Signals, Systems and Computers, Pacific Grove, CA, USA, November 2003.


[2] J. Ascenso, P. Akayzi, M. Testolina, A. Boev, E. Alshina “Performance Evaluation of Learning based Image Coding Solutions and Quality Metrics”, ISO/IEC JTC 1/SC29/WG1 N85013, 85th JPEG Meeting, San Jose, USA, November 2019. Available [here](https://jpeg.org/items/20191203_jpeg_ai_performance_evaluation.html).


[3] Z. Li, A. Aaron, I. Katsavounidis, A. Moorthy and M. Manohara, “Toward A Practical Perceptual Video Quality Metric”, [Online], Available [here](https://netflixtechblog.com/toward-a-practical-perceptual-video-quality-metric-653f208b9652).


[4] H.R. Sheikh and A. C. Bovik, “Image Information and Visual Quality,” IEEE International Conference on Acoustics, Speech, and Signal Processing, Montreal, Canada, August 2004.


[5] L. Zhang, L. Zhang, X. Mou, D. Zhang, “FSIM: a Feature Similarity Index for Image Quality Assessment,” 
IEEE Transactions on Image Processing, vol. 20, no. 8, pp. 2378-2386, August 2011.


[6] V. Laparra, J. Ballé, A. Berardino, and E. P. Simoncelli, “Perceptual Image Quality Assessment using a Normalized Laplacian Pyramid”, S&T Symposium on Electronic Imaging: Conf. on Human Vision and Electronic Imaging, San Francisco, CA, USA, February 2016.