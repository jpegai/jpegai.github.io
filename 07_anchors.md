---
layout: page
title: Anchors
permalink: /7-anchors/
---

### Anchors

Proposals will be compared against the following anchors:

* JPEG (ISO/IEC 10918-1 \| ITU-T Rec. T.81)
* JPEG 2000 (ISO/IEC 15444-1 \| ITU-T Rec. T.800)
* HEVC Intra (ISO 23008-2 \| ITU-T Rec. H.265)

Information on available software and configurations to be used for these anchors is given in Annex C.


The configurations detailed below are relevant for the definition of anchors.

### JPEG (ISO/IEC 10918-1 \| ITU-T Rec. T.81))
JPEG does not specify a rate allocation mechanism allowing to target a specific bitrate. Hence, an external rate control loop is required to achieve the targeted bitrate. The following conditions apply:
* Software to be used: JPEG XT reference software, v1.53
	+ Available [here](http://jpeg.org/jpegxt/software.html)
	+ License: GPLv3
* Command-line examples (to use within the rate-control loop): jpeg -q [QUALITY_PARAMETER] [INPUTFILE] [OUTPUTFILE]


### JPEG 2000 (ISO/IEC 15444-1 \| ITU-T Rec. T.800)
The JPEG 2000 anchor generation should support two configurations: 1) PSNR optimized; and 2) Visually optimized. A target rate can be specified using the –rate [bpp] parameter. The following conditions apply:
* Software to be used: Kakadu, v7.10.2
	+ Available [here](http://www.kakadusoftware.com)
	+ License: demo binaries freely available for non-commercial use
* Command-line examples: 	
	+ **MSE weighted**: kdu_compress -i [INPUTFILE] -o [OUTPUTFILE] -rate [BPP] Qstep=0.001 -tolerance 0 -full -precise
	+ **Visually weighted**: kdu_compress -i [INPUTFILE] -o [OUTPUTFILE] -rate [BPP] Qstep=0.001 -tolerance 0 -full -precise -no_weights
	+ **Decoding**: kdu_expand -i [INPUTFILE .mj2] -o [OUTPUTFILE .yuv] -precise


###	HEVC (ISO 23008-2:2018 \| ITU-T Rec. H.265 (v5))
For HEVC, an external rate control loop is required to achieve targeted bitrate. The HEVC RD performance for the target bitrates are obtained with the following conditions:
* Available software: HEVC Test Model HM-16.20+SCM-8.8
	- Available [here](https://hevc.hhi.fraunhofer.de/svn/svn_HEVCSoftware/tags/HM-16.20+SCM-8.8/ )
	- License: BSD
* FFMPEG will be used to convert the PNG (RGB) to YUV files following the BT.709 primaries.
	- ffmpeg -hide_banner -i input.png -pix_fmt yuv444p10le -vf scale=out_color_matrix=bt709 -color_primaries bt709 -color_trc bt709 -colorspace bt709 -y output.yuv
* Configuration files to be used are available [here](/public/encoder_intra_main_scc_10.cfg)

