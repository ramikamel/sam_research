# PixelPerfect

## Overview

Segmentation models are known for their effectiveness with clear and distinct images. However, the Segment Anything Model (SAM) claims to maintain high accuracy even with ambiguous objects or overlapping features. Our project, Pixel Perfect, aims to put this claim to the test by focusing on the segmentation of pneumonia-affected regions in lung X-ray images. We will train and evaluate a model based on SAM, applying advanced image preprocessing techniques to enhance its performance in segmenting pneumonia. By refining images before analysis, we aim to improve the delineation of pneumonia-affected areas, advancing the capabilities of current segmentation models and pushing the boundaries of segmentation in the medical realm.

## Image Segmentation 

How Does it Work?
Image segmentation consists of 3 primary steps:
Feature Extraction: The first step involves extracting meaningful features from the image. These features can include color, texture, edges, or shape information.
Grouping: Once features are extracted, they are grouped together based on similarity. This can be done using techniques like clustering or thresholding.
Boundary Refinement: The boundaries of the segmented regions are often refined to ensure they accurately represent the objects in the image. This might involve smoothing edges or removing small, noisy regions.

## Preprocessing Methodology

- **Canny Edge Detection (CED):** CED identifies clear, continuous edges by smoothing the image and filtering pixels based on thresholding and edge connectivity.
- **CLAHE:** CLAHE enhances image contrast by dividing an image into small regions, applying histogram equalization to each, and limiting contrast to reduce noise.
- **Gaussian Blur:** Gaussian blur reduces noise by averaging pixel values with a function gives more weight to central pixels in a specified neighborhood.
- **Entropy and SSIM:** The entropy and SSIM optimization were used to maximize information content by adjusting image features to enhance clarity and still preserve each image’s structural information.

*X-ray after preprocessing methodology:*


<img src="https://github.com/erm1na/PixelPerfect/blob/main/images/Screenshot%202024-11-17%20202644.png" alt="Alt text" width="450"/>

*SAM contoured image:*


<img src="https://github.com/erm1na/PixelPerfect/blob/main/images/Screenshot%202024-11-17%20202709.png" alt="Alt text" width="450"/>

## Features

- **Image Preprocessing:** Utilize image preprocessing methods to help SAM identify pneumonia through potentially ambiguous lung X-rays.
- **Training SAM:** Feed our preprocessed images through SAM and measure confidence/accuracy.
- **Bounding Boxes Generator:** Generate bounding boxes around SAM-generated masks.
- **Data Evaluation:** Calculate confidence scores and SAM consistency scores.

## Installation and Use

The notebooks are best run separately in Google Co-lab. Certain notebooks may require a higher GPU usage.

## Results
<img src="https://github.com/erm1na/PixelPerfect/blob/main/images/Screenshot%202024-11-17%20194442.png" alt="Alt text" width="450"/>
<img src="https://github.com/erm1na/PixelPerfect/blob/main/images/Screenshot%202024-11-17%20194500.png" alt="Alt text" width="450"/>
<img src="https://github.com/erm1na/PixelPerfect/blob/main/images/Screenshot%202024-11-17%20194514.png" alt="Alt text" width="450"/>
<img src="https://github.com/erm1na/PixelPerfect/blob/main/images/Screenshot%202024-11-17%20194526.png" alt="Alt text" width="450"/>



## Conclusion

We found that, by employing image preprocessing and model training techniques,
we can improve SAM’s accuracy and consistency, thus enhancing its ability to be
effectively applied to medical imaging contexts. We found that that by employ‐
ing image preprocessing and model training techniques. However, the presence
of numerous outliers suggests that further fine‐tuning is necessary. The results
demonstrate the potential for optimized preprocessing and training protocols to
improve the model’s performance in clinical settings.
