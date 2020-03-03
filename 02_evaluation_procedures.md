---
layout: page
title: Evaluation Procedure
permalink: /2-eval_proc/
---

Objective and subjective quality evaluation of the proposals will each be done by at least two independent labs, following well-established procedures and based on the decoded test images provided by each proponent. The submitted code (or binaries) for the decoder, codestreams and decoded images will be used for verification purposes. In the figure bellow, the coding pipeline for learning-based image coding solutions, which is rather straightforward, is presented. Proponents may perform encoding with any color space representation, but the input of the encoder and the output of the decoder must be in the PNG (RGB color space) format. Objective image quality will be measured with luminance and color-based metrics and the RGB decoded images will be used for quality evaluation.

<p align="center">
<img src="/public/pipeline.svg" width="600" height="300" alt="Coding pipeline"/>
</p>

### Target rates

Target bitrates for the objective evaluations include **0.06, 0.12, 0.25, 0.50, 0.75, 1.00, 1.50, and 2.00 bpp**. The maximum bitrate deviation from the target bitrate should not exceed **15%**. The proponents must declare for every test image which target bitrate their decoder and models can reach, and in case of deviation of the target bitrate, the proposed RD point may not be considered for evaluation. The target bitrates for the subjective evaluations will be a subset of the target bitrates for the objective evaluations and will depend on the complexity of the test images.
The bitrates specified should account for the total number of bits necessary for generating the encoded file (or files) out of which the decoder can reconstruct a lossy version of the entire image. The main rate metric is the number of bits per pixel (bpp) defined as:


BPP = (N_TOT_BITS)/(N_TOT_PIXELS)


where N_TOT_BITS is the number of bits for the compressed representation of the image and N_TOT_PIXELS is the number of pixels in the image. 


### Objective quality testing

Objective quality testing shall be done by computing several quality metrics, including MS-SSIM, VMAF, VIFP, NLPD, FSIM, between compressed and original image sequences, at the target bitrates mentioned in the precious Section. Refer to Annex C for more information about the image quality metrics.

### Subjective quality testing

To evaluate the selected coding solutions, a subjective quality assessment methodology may be used. This type of assessment is especially critical since the type of artifacts that learning-based image compression solutions produce may be significantly different from those in standard image codecs. Subjective quality evaluation of the compressed images will be performed on the test dataset. 

The Double Stimulus Impairment Scale (DSIS) methodology will be used, where subjects watch side by side the original image and the impaired decoded image which is scored in a 1-5 scale associated to five impairment scale, notably very annoying, annoying, slightly annoying, perceptible but not annoying and imperceptible. The side-by-side images are centered on the display. The reference is shown on the left or right and can vary randomly. Subjects will be informed that one of the images is the reference but will not receive any indication whether the reference image was on the left or on the right. 

The subjective test methodology will follow BT500.13 [1] and a randomized presentation order, as described in ITU-T P.910 [2] will be used; the same content is never displayed consecutively. There is no presentation or voting time limit. A training session should be organized before the experiment to familiarize participants with artefacts and distortions in the test images. At least, three training images will be used before actual scoring.

As anchors, JPEG, JPEG 2000 and HEVC will be used. The list of anchors may be reduced if the number of proposals is too high. The images used for subjective evaluation are a subset of the test dataset images and its number will be selected depending on the number of proposals that will be subjectively evaluated. 

### References

[1] ITU-R Recommendation BT.500-13, “Methodology for the subjective assessment of the quality of television pictures,” International Telecommunications Union, Geneva, Switzerland, 2012.


[2] ITU-T Recommendation P. 910, “Subjective video quality assessment methods for multimedia applications,” International Telecommunication Union, Geneva, 2008.




