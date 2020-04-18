---
layout: page
title: Submission Requirements
permalink: /2-sub_req/
---

Proponents are expected to compress some test material to be provided, with their codec using some target bitrates described in the [evaluation procedure](/2-eval_proc/). The [datasets](/1-datasets/), [quality metrics](/3-metrics/) and [anchors](/4-anchors/) are also available.

### Proposal description

Each proposal must include a technical description of the entire image codec, in the form of a 2-column paper (using the MMSP paper template and submission rules), namely:
* Key features of the proposal, including the target quality range.
* High-level description of the proposal.
* Encoder/decoder architecture, training procedure including loss function used, strategies on how to deal with the non-differentiable quantization and bitrate allocation.
* Model size if applicable, which corresponds to the number of weights (and precision of each weight) in the encoder and decoder.
* RD performance for at least four test images (to be specified) using MS-SSIM and VMAF objective metrics. 
* Time duration of encoding and decoding processes:
	* Information about the processor platforms used, including the type of platform (e.g. CPUs, GPUs, ASIC-based accelerators, FPGAs, etc.), brand, CPU model, number and clock rate of cores, size of on-chip memory, size of main memory, model of ML/graphic accelerators (e.g. model of GPU card).
	* ML framework (e.g. Caffe, Tensorflow, MindSpore, Pytorch) and its version information.
	* ASIC-based, FPGA-based accelerators and new ML frameworks are encouraged to be used (if used then should be clearly specified).

Participants may decide to submit the description of their coding solutions in different ways:
1. JPEG technical document,
2. MMSP paper following the MMSP2020 submission guide lines and according to the MMSP2020 paper kit (although not by the same deadline),
3. JPEG technical document and a MMSP 2020 submission.

### Additional elements
The following additional elements must be submitted by all proposals:
* Standalone executable package: docker file with all the libraries and tools to run the decoder with the submitted code-streams and preferably decoder in source code form. All the information to run the decoder shall be provided. If binaries are used, they should correspond to statically linked Linux executables with all required libraries and system dependencies
* Code-streams corresponding to the encoded test images to be used for decoding.
* Decoded test images for objective and subjective evaluation. All test images will be made available to proponents on the website created for the Call for Evidence (and Challenge). 
* Training dataset (if the JPEG AI dataset was not used). This is optional.

Decoded images should be sRGB with 8 bits per component. Contributors are also expected to provide to the JPEG committee sufficient rights to allow usage of the provided software for the purpose of evaluation. The evaluation process may need to crop and/or clip the provided images to make them suitable for subjective evaluation. 

### Standardization process
In addition to the technical description and the additional elements (code or binaries, decoded images, etc) to be submitted, proponents are encouraged to contribute to the standardization process, namely by participating in the JPEG AI ad-hoc group:
* E-mail reflector: [jpeg-ai@jpeglists.org](jpeg-ai@jpeglists.org)
* To subscribe to the reflector, please visit [JPEG AI mailing list](http://jpeg-ai-list.jpeg.org) or in case of problems contact [us](mailto:lists@jpeg.org).
