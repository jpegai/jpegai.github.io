---
layout: page
title: Submission instructions and reporting guidelines
permalink: /sub_instructs/
---

## Test images
The test images will be available here.


## Docker file 
To ensure the proponents computing environment (to run your submitted decoder) can be reproduced, a Dockerfile is required as part of the full submission.

To configure a suitable environment, it is proposed to start from one of the following Docker images: 
- [tensorflow](https://hub.docker.com/r/tensorflow/tensorflow)
    * tensorflow/tensorflow:1.15.0-gpu-py3 (GPU)
    * tensorflow/tensorflow:1.15.0-py3 (CPU)
    * tensorflow/tensorflow:2.0.0-gpu-py3 (GPU)
    * tensorflow/tensorflow:2.0.0-py3 (CPU)
- [pytorch](https://hub.docker.com/r/pytorch/pytorch)
    * pytorch/pytorch:1.3-cuda10.1-cudnn7-runtime (GPU)

The decoder must be able to run in either one of the above listed Docker images or an image specified on your own. In either case, a Dockerfile that allows for replication of your environment must be part of the full submission.

For instructions on how to work with Docker we recommend the official [documentation](https://docs.docker.com/).


## Memory requirements
Report the amount of memory and GPU model required for decoding (inference) [here](https://forms.gle/MB8JG2LF383Jgaza7).


## Bitrate reporting and cross-check verification
The following information is needed for all decoded test images:
* Target and real bitrates.
* Mean Square Error (MSE) using the corresponding original image as reference.

The proponents should use the CSV template available [here](link_to_csv).

## Decoded images naming convention 
The decoded files must be performed according to the following naming convention: `<TEAMID>_<IMGID>_TE_<RES>_8bit_sRGB_<BR>.png`
    * TEAMID is the registration team ID attributed with 2 digits
    * IMGID is an identification of the image with 5 digits
    * TE is a fixed value which represents it is a test image
    * RES is the spatial resolution (width x height)
    * Bit depth (which must be 8 bits always)
    * Color space (which must be sRGB)
    * BR target bitrate for decoded images: YXX (e.g. 1.25 bpp would be ‘125’ and 0.05 would be 005)


## File submission
The submission must be performed by using sftp according to the following instructions.
* The access to the FTP site should be performed with [FileZilla](https://filezilla-project.org/)  
* Protocol: FTP 
* Host (FTP sever): tremplin.epfl.ch .
* Username: <USER>@mmspgdata.epfl.ch 
* Password: <PASSWORD>
* FTP port: 21 

NOTE: The username includes "@mmspgdata.epfl.ch" 

The USER/PASSWORD will be sent to you by email.


There should be four seperate ZIP files with the following information:
* Decoder+docker file: source decoder and docker configuration file. If justified, the Docker container could be considered for submission.
* Model(s) to be used during decoding. The following naming convention must be used: `<TEAMID>_<BR>.model`. If only one model is used <BR> should be set to 'all'. 
* Bitstreams to be used for decoding using the same naming convention as the decoded images but with .bits extension.
* Decoded images according to the naming convention above.

The naming convention for the zip files is `TEAMID_DATETIME_<[Decoder+docker file | Models | Bitstream | Decoded]>.zip
