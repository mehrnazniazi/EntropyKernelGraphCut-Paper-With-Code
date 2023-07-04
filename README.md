# EntropyKernelGraphCut-Paper-with-Code
Entropy-based Kernel Graph Cut for Textural Image Region Segmentation

This repository contains an implementation of the Entropy-based Kernel Graph Cut algorithm for textural image region segmentation. While the RBF kernel graph cut algorithm is effective for general image segmentation, it falls short when applied to textural images due to its reliance on intensity variation and smoothness attributes of the RBF kernel function. To address this limitation and handle image complexity, we introduce an entropy-based kernel function that leverages the advantages of implicit mapping.

Entropy is a random measurement statistic and can be used to quantify local and geometrical features of an image. It can be used to describe the structural information of the local intensity of the input image with efficient computational cost. In this regard, grayscale image histogram h is calculated and normalized through image size and replaced by the corresponding pixel value in the image. Then, entropy features are calculated over the entire image pixels per window of size m×m and rescaled within the range of 0-255. Finally, the feature matrix F is reconstructed with the combination of entropy grayscale image E ́ and basic grayscale image G as shown in Figure. Consequently, 2-layer feature space (1-layer gray level and 1-layer entropy feature) can be incorporated into a segmentation method to make it more efficient for textural images

Entropy-based kernel graph cut has computed local correlation due to its window-scanning in compare to RBF kernel graph cut in which spatial correlation is computed in general. Moreover, unlike the RBF method that is highly dependent on spatial distance based on intensity values clustering, entropy-based kernel graph cut method is independent of spatial properties and depend on the pixel’s brightness. 


If you find this work useful in your research, please consider citing the following paper:

M. Niazi, K. Rahbar, M. Sheikhan, and M. Khademi, "Entropy-based kernel graph cut for textural image region segmentation," Multimed. Tools Appl., vol. 81, no. 9, pp. 13003–13023, Apr. 2022.

You can access the paper at 
https://link.springer.com/article/10.1007/s11042-022-12005-z
