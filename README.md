# Radiomics-on-BRATS-Dataset

This project has been conducted in order to find and classify potential tumours inside the BRATS dataset. 

The BraTS dataset (Brain Tumor Segmentation) is a dataset used in medical imaging for brain tumor segmentation.
The focus of BraTS is on gliomas, a category of brain tumors that includes both low-grade gliomas (LGG) and highly malignant high-grade gliomas (HGG).
Here are reported some specifics:

- MRI scans:
    T1: T1-weighted, providing detailed anatomical information.
    T1ce: T1 with contrast enhancement, highlighting tumor regions.
    T2: T2-weighted, useful for visualizing edema and fluid.
    FLAIR: Fluid-Attenuated Inversion Recovery, for visualizing edema and abnormalities.

- LABLES:
    0: Healthy tissue (no tumor).
    1: Necrotic and Non-enhancing Tumor Core.
    2: Edema.
    4: Enhancing Tumor Core.

  - 67 PATIENTS
 
This processing part is focused on managing, preprocessing, and generating data for training ML models for 3D medical images segmentation.

Key operations include:
1.   Separating ground truth data from images.
2.   Normalizing the images, developing stategies like gaussian distribution on voxels, a min-max normalization and a median-based normalization.
3.   Applying data augmentation techniques (flipping) to increase data variability and improve the model's generalization.
4.   Creating a data generator that provides:
5.   A tensor for the input images (image_tensor).
6.   A tensor for the ground truth labels (truth_tensor).
