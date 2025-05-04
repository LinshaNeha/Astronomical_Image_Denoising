# Astronomical_Image_Denoising

Astronomical Image Denoising using Classical Techniques

This project focuses on enhancing the quality of astronomical images by applying various classical denoising techniques. It aims to remove noise and restore visual clarity using methods like BM3D, Wavelet Thresholding, Non-Local Means (NLM), and Bilateral Filtering.

Problem Statement

Astronomical images often suffer from noise due to atmospheric interference, sensor limitations, and long exposure times. This noise can obscure important details necessary for analysis. The goal of this project is to compare the effectiveness of different classical denoising techniques in restoring these images with minimal loss of important information.



Team Members

| Name                |
|---------------------|
| Ashlin Rodrigues    | 
| Linsha Neha Bangera | 
| Sweedal Grace Pinto |


Dataset Used

- NASA Image of the Day Dataset
- A curated collection of astronomical images published by NASA.
- These images serve as input for various denoising techniques applied in this project.


Techniques Implemented
 1.  BM3D (Block-Matching and 3D Filtering)
- Best at preserving edges and textures.
- Groups similar blocks and applies collaborative filtering in a 3D transform domain.
 2.Wavelet Thresholding
- Decomposes the image into frequency bands.
- Applies soft thresholding to remove noise while preserving signal.
- Reconstruction using inverse wavelet transform.

 3.Non-Local Means (NLM)
- Averages pixels with similar neighborhoods.
- Strong in preserving fine details and repetitive textures.

 4.Bilateral Filtering
- Smoothens the image while keeping edges sharp.
- Considers both spatial proximity and pixel intensity difference.


Evaluation Metrics

Each denoising method is evaluated using:

- PSNR (Peak Signal-to-Noise Ratio)
- SSIM (Structural Similarity Index)
- MSE (Mean Squared Error)
- mIoU (Mean Intersection over Union)


Program Flow

1. Load images from the dataset.
2. Convert each image from BGR to RGB.
3. Apply the following denoising methods:
   - bm3d_denoise()
   - wavelet_denoise()
   - nlm_denoise()
   - bilateral_filter_denoise()
4. Evaluate and print PSNR, SSIM, MSE, and mIoU.
5. Create and save a collage of original + denoised images.
6. Display the result for the first 10 images using `matplotlib`.



Platform Used

- Jupyter Notebook
- Python Libraries:
  - OpenCV
  - scikit-image
  - scikit-learn
  - bm3d
  - pywavelets
  - matplotlib
  - numpy



Installation

Run the following to install dependencies:

bash
pip install scikit-image scikit-learn opencv-python-headless matplotlib bm3d pywavelets

