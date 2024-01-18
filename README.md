# **Monocular depth estimaion on outdoor environment**

Monocular depth estimation is an important task in computer vision that aims to predict three-dimensional depth information from a single two-dimensional image. A long-standing challenge in computer vision has been monocular depth estimation, which has critical implications for robotics, autonomous driving, and augmented reality. The dissertation examines the application and evaluation of Fully Convolutional Residual Networks (FCRN) in monocular depth estimation, a critical task in computer vision involving predicting the depth of a scene based on one input image. Providing a realistic but computationally manageable benchmark for the experiments, the study uses a subset of a larger dataset. The FCRN model exhibits promising results, demonstrating a competitive level of accuracy in depth prediction across diverse environmental settings despite not achieving state-of-the-art performance. This research contributes to ongoing efforts in computer vision by shedding light on the capabilities and limitations of FCRN architectures for monocular depth estimation tasks and suggests avenues for future improvements. 
Although the dissertation's primary focus remains on the application of the FCRN model, it also examines the inherent challenges associated with monocular depth estimation. Using multiple viewpoints or special sensors is often necessary to gauge depth, but the goal is to do so with a single RGB image, increasing the system's utility and applicability. By training and evaluating the model on a subset of the KITTI dataset, a high-quality dataset representative of real-world situations is used. Although the proposed FCRN model performs at a level close to state-of-the-art, it also highlights the room for improvement and sets the stage for future research to enhance its predictive accuracy and computational efficiency.

## **Usage**
In order to run the code, simply open the google colab file and run all cells. Please note that all the dataset files are downloaded from google drive. In order to inpaint the images please follow the process mentioned in the notebook. The inpainting process requires alot of GPU and time. So its better to use local system (if the GPU and processor is good) in order to perform inpainting on the kitti dataset. 


## **Dataset**
Machine learning models need to be trained and evaluated using an appropriate dataset, especially monocular depth estimation models. The KITTI (Karlsruhe Institute of Technology and Toyota Technological Institute) dataset has been selected as the primary resource for this study. The KITTI dataset is a benchmark suite specifically designed to advance the field of autonomous driving, offering a rich set of high-quality data samples that are pertinent to various computer vision tasks. 
https://www.cvlibs.net/datasets/kitti/

## **Inpainting**
The annotated depth data acquired from KITTI dataset is sparse point clouds, unlike the dense depth maps its missing few pixel. In order to convert sparse point clouds into complete depth maps the framework performs inpainting or filling. Inpainting algorithms to fill in any missing or noisy depth information are applied by using a guided filter-based inpainting technique that considers both depth and RGB images. The in-painted depth maps aim to remove noise and improve the quality of depth data. The method of inpainting was inspired by Alhashim el al. code in order to perform inpainting on both NYU and KITTI dataset. 
https://arxiv.org/abs/1812.11941

## **Framework**
The main model architecture: 
![IMG_0393 (1)](https://github.com/kadilrahman/Depth-estimation-FCRN-/assets/80009565/283c8416-1d6c-463b-92f5-419d0699db27)


ResNet structure:
![IMG_0398](https://github.com/kadilrahman/Depth-estimation-FCRN-/assets/80009565/15ce0065-a0d8-43ef-8d73-8d5668bcf475)

## **Check Results and code in google colab document**
https://colab.research.google.com/drive/1aZxx88Lnawrxd2hKXMXHeSxL_FIHdygk?usp=sharing

