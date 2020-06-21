---
layout: page
title: JPEG AI Datasets
permalink: /3-datasets/
---

The JPEG AI database was constructed to (i) evaluate the performance of state-of-the-art 
learning-based image coding solutions, and (ii) to be used for training, validation and 
testing of novel learning-based image coding solutions. This dataset will be made available 
to all participants to the Challenge. The JPEG AI dataset will be organized according to:

* Training dataset: The training dataset aims to provide a set of images to create a model 
suitable for a learning-based image codec solution. However, the proponents may also use a 
different training dataset provided that it is fully identified in the proposal description 
and, ideally, made available for future developments.

* Validation dataset: The validation dataset aims to provide a set of images to be used during 
the training to validate the convergence of the training algorithm used by some 
learning-based image codec solution.

* Test dataset (hidden): The test dataset cannot be used neither for training nor validation and 
will be used to evaluate the final performance of learning-based image coding solutions. Test images 
are kept hidden until some appropriate stage, to avoid being used for training. The test dataset 
for the evaluation of the Challenge submissions will be drawn from a sizeable repository 
that is maintained by JPEG.

## JPEG AI Dataset Characterization

The diversity of the images contained in the JPEG AI dataset is high, namely in terms of their 
characteristics, such as content and spatial resolution. These datasets have the following characteristics:

* Format: PNG images (RGB color components, non-interlaced);
* Spatial resolution: from 256×256 to 8K (8 bit);
* Training/validation dataset: 5264/350 images.

The numbers of images above allow for an efficient training/validation and they are typically larger than 
the numbers used in available works. The number of test images provides a 
well-balanced set of diverse images that can be used for a representative evaluation of 
learning-based image coding solutions. The training and validation dataset will be available 
[sftp://jpeg-cfe@amalia.img.lx.it.pt]() (password to be given by request) by 10th March, 2020.

