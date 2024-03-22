# Is It My Mom or Me? - Image Similarity Analysis

This project aims to determine how much individuals resemble their parents, specifically focusing on visual similarities between my and my mom. It uses various Python libraries to process images, detect faces, and compute similarity scores.
Overview

The code performs the following operations:

*  Image Processing: Converts images to a consistent format and crops faces from the images using OpenCV.
* Feature Extraction: Utilizes a pre-trained Vision Transformer (ViT) model from the transformers library to extract image features.
* Similarity Calculation: Computes the cosine similarity between feature vectors of the processed images to quantify resemblance.
* Image Comparison: Analyzes sets of images, comparing each image of the child ('cris') with those of the mother ('mom'), to find the pair with the highest and lowest similarity scores.

### Dependencies

* torch: For deep learning operations and handling tensors.
* transformers: To load pre-trained models for feature extraction
* opencv-python (cv2): For image processing tasks such as reading images and face detection.
* PIL (Pillow): For image manipulation like cropping and converting image formats.
* fastai: For additional image processing utilities.
* numpy: For numerical operations.

### Key Functions

```markdown
crop_image(im_for_crop): Detects and crops the face from an image.
```
```markdown
    get_similarity(file_name1, file_name2): Calculates the similarity score between two images.
```
```markdown
    show_images(rows, cols, imgs, labels, size=(256, 256)): Displays a grid of images with labels, useful for visualizing the results.
```

<img width="367" alt="Screenshot 2024-01-21" src="https://raw.githubusercontent.com/Yosolita1978/screenshoots/c848fbd32de0317496264ca36c67e169907441ba/2024/AI/Screen%20Shot%202024-03-21%20at%205.38.41%20PM.png">

### Workflow

1. Face Detection: Each image is processed to detect and crop the face, ensuring that comparisons focus on facial features.

2. Feature Extraction: Faces are analyzed using the ViT model to extract feature vectors.

3. Similarity Scoring: Calculates the similarity between each pair of images (child and mother) to find the most and least similar pairs.

4. Result Visualization: Displays the images with the highest and lowest similarity scores, along with a grid of selected images for quick comparison.

### Conclusion

This tool provides a fun and insightful way to explore familial resemblance through image analysis, demonstrating the power of machine learning and image processing in personal contexts.