---
layout: page
title: Submission Requirements
---

In addition to the technical description and other elements (code or binaries, decoded images, etc) to be submitted, proponents are encouraged to contribute to the standardization process, namely by participating in the JPEG AI ad-hoc group.

### Proposal description

Each proposal must include a technical description of the entire image codec, in the form of a 2-column paper (using the MMSP paper template and submission rules), namely:
* Key features of the proposal, including the target quality range.
* High-level description of the proposal.
* Encoder/decoder architecture, training procedure including loss function used, strategies on how to deal with the non-differentiable quantization and bitrate allocation.
* Model size if applicable, which corresponds to the number of weights (and precision of each weight) in the encoder and decoder.
* RD performance for at least four test images (to be specified) using MS-SSIM and VMAF objective metrics. 
* Running time (encoder and decoder) for some CPU and GPU platform. Include all the details of the platform (CPU model, clock rate and memory, GPU model and brand) but also the deep learning framework (e.g. Tensorflow or Pytorch). The recommended platform for GPU is NVIDIA 2080 Ti, but you may use other one. 


### Additional elements
The following additional elements must be submitted by all proposals:
* Standalone executable package: docker file with all the libraries and tools to run the decoder with the submitted code-streams and preferably decoder in source code form. All the information to run the decoder shall be provided. If binaries are used, they should correspond to statically linked Linux executables with all required libraries and system dependencies
* Code-streams corresponding to the encoded test images to be used for decoding.
* Decoded test images for objective and subjective evaluation. All test images will be made available to proponents on the website created for the Call for Evidence (and Challenge). 
* Training dataset (if the JPEG AI dataset was not used). This is optional.
