# TFM_VIU_BIG_DATA
TFM name: Image restoration using transformers
Autor: Walter Bustillo Barrientos

The present has as its main objective the restoration of images applying models based on Transformers and as a secondary objective the reduction of the computational resorces of a Transformers model by replacing the MultiHead attention module with a Pooling module.

State of art:
- https://github.com/ZhendongWang6/Uformer
- https://github.com/sail-sg/poolformer
- https://github.com/juglab/pn2v

Update: 
- 2022.19.05 The codes will be upload and the results.

The present has as its main objective the restoration of images applying models based on Transformers and as a secondary objective the reduction of the computational resorces of a Transformers model by replacing the MultiHead attention module with a Pooling module.
The first step is to analyze the Transformers models, based on the project developed by Zhendong Wang called Uformer: A General U-Shaped Transformer for Image Restoration (Wang, Uformer: A General U-Shaped Transformer for Image Restoration, 2021) which proposes an image restoration model based on a U-Net architecture and replacing convolutional modules with Transformers modules.
The Zhendong Wang model will be used, developed in the Python programming language to be able to work on any computer that has a development interpreter and has a GPU. We will apply the models established in Google Colab, a collaborative environment that works with Notebooks, which is interpreted in the cloud, in addition to having the option of using a GPU that works with the Python programming language.
To carry out the training and evaluation of the model, three different databases will be used to execute the model. The first database will be the same used in the previously mentioned work (Wang, Uformer: A General U-Shaped Transformer for Image Restoration, 2021). The second and third databases will be obtained from the work carried out by Alex-Krull called Probabilistic Noise2Void: Unsupervised Content-Aware Denoising (Krull, Vicar, Prakash, Lalit, & Jug, 2020)databases which are called Convallaria and Confocal_MICE.
Then, a variation will be made to the original model based on the work carried out by Weihao Yu called 'MetaFormer is Actually What You Need for Vision' (Yu, 2021) in which he proposes a solution with a more adequate architecture in computational resources to replace the Transformers. In order to simplify the architecture, a change is made in the self-service module of the Transformers for a module made up of Pooling layers. The work carried out shows more efficient results when changing modules, which will be implemented in the development of the proposed work to see the behavior with the Uformer architecture.
In the development of this work, a change is made in the architecture of the W/MW-MSA module, which is a MultiHead service model, for a Pooling module, described in the previously mentioned work, when making this change, they again use the same databases and do not change parameters to be able to make comparisons between the results obtained by both models.
The results obtained through the implementation of this project are evaluated with the PSNR and SSIM metrics, metrics used for image quality, which will support the results obtained, one aspect to take into account during the development is to note that the base data used in the work of Zhendong Wang was inconclusive due to the lack of computational resources, revealing the limitations of working with a developer in the cloud.

# Results

## Uformer

Convallaria
![image](https://user-images.githubusercontent.com/91577811/169423969-8e00be4d-2c1e-446e-b6a9-4a07583f5c24.png)

Confocal_MICE
![image](https://user-images.githubusercontent.com/91577811/169424050-5b597de7-58c1-45b8-99df-74f07f3b0f1b.png)

## Poolformer

SSID
![image](https://user-images.githubusercontent.com/91577811/169423025-3228ebd3-e24b-4c17-b426-b33de99f8303.png)

Convallaria
![image](https://user-images.githubusercontent.com/91577811/169424149-93c326f7-be19-494e-b0d4-ae670e4b41f5.png)

Confocal_MICE
![image](https://user-images.githubusercontent.com/91577811/169424092-8c588546-09ab-4d81-8870-227ae2e8253a.png)


