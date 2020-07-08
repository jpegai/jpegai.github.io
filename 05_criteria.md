---
layout: page
title: Assessment Criteria
permalink: /5-criteria/
---

A set of common test conditions (CTC) for learning-based image codecs was designed in the context of the JPEG AI activities, which defines training and testing datasets, benchmarking codecs, coding conditions (especially target bitrates) and a set of reliable objective quality metrics and subjective assessment procedures [1]. This CTC allows to exhaustively evaluate multiple aspects of learning-based image codecs to fully understand their strengths and weaknesses, notably regarding already available image coding technology. 

The Challenge (and Call for Evidence) evaluation process will be based on the JPEG AI CTC and will focus mostly on compression performance. There are three types of criteria that will be used for the evaluation of the submissions:
* Objective evaluation with quality metrics including at least MS-SSIM, VMAF, VIFP, NLPD, FSIM which have been shown to provide high correlation [2] with perceptual assessment for learning-based image codecs. 
* Subjective evaluation to be performed with a double stimulus (DSIS) protocol, thus collecting MOS values. These tests will be made in a controlled environment, following well-defined procedures established by ITU standards.

For the subjective testing to be manageable, it is possible that not all submitted proposals will be selected for final subjective performance evaluation. The selection will involve a first assessment stage using a set of objective metrics which should allow to find the top performing submissions. After the identification of the highest RD performance submissions (by measuring distortions objectively) and a review of the technical contributions and relevance of each one considering the Call for Evidence objective, some proposals will be selected to be evaluated with an appropriate subjective evaluation procedure (2nd stage). 

From the subjective assessment tests, the top performing solutions will be drawn, not only considering the subjective performance (including confidence intervals, target bitrates for which have been superior) but also the novelty, complexity and relevance regarding the Challenge (and Call for Evidence) objective and complexity. 

In addition to the selected submitted image codecs, the quality evaluation will also include well-known standardized image coding solutions such as JPEG, JPEG 2000 and HEVC.

The selection of the proposals for subjective assessment will be made by a Selection Board constituted by the Challenge organizers, the JPEG Coding, Test and Quality sub-group chairs (Peter Schelkens and Thomas Richter) and the MMSP challenge chair (Jiaying Liu).


## References

[1] J. Ascenso, P. Akayzi “JPEG AI Image Coding Common Test Conditions”, ISO/IEC JTC 1/SC 29/WG 1 N84035, 84th Meeting, Brussels, Belgium, 13-19 July 2019.


[2] J. Ascenso, P. Akayzi, M. Testolina, A. Boev, E. Alshina “Performance Evaluation of Learning based Image Coding Solutions and Quality Metrics”, ISO/IEC JTC 1/SC29/WG1 N85013, 85th JPEG Meeting, San Jose, USA, November 2019. Available [here](https://jpeg.org/items/20191203_jpeg_ai_performance_evaluation.html).


