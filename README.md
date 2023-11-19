# Image Restoration Via Frequency Selection

Yuning Cui, Wenqi Ren, Xiaochun Cao, and Alois Knoll

>Image restoration aims to reconstruct the latent sharp image from its corrupted counterpart. Besides dealing with this longstanding task in the spatial domain, a few approaches seek solutions in the frequency domain by considering the large discrepancy between spectra of sharp/degraded image pairs. However, these algorithms commonly utilize transformation tools, e.g., wavelet transform, to split features into several frequency parts, which is not flexible enough to select the most informative frequency component to recover. In this paper, we exploit a multi-branch and content-aware module to decompose features into separate frequency subbands dynamically and locally, and then accentuate the useful ones via channel-wise attention weights. In addition, to handle large-scale degradation blurs, we propose an extremely simple decoupling and modulation module to enlarge the receptive field via global and window-based average pooling. Furthermore, we merge the paradigm of multi-stage networks into a single U-shaped network to pursue multi-scale receptive fields and improve efficiency. Finally, integrating the above designs into a convolutional backbone, the proposed Frequency Selection Network (FSNet) performs favorably against state-of-the-art algorithms on 20 different benchmark datasets for 6 representative image restoration tasks, including single-image defocus deblurring, image dehazing, image motion deblurring, image desnowing, image deraining, and image denoising.

## Installation
The project is built with PyTorch 3.8, PyTorch 1.8.1. CUDA 10.2, cuDNN 7.6.5
For installing, follow these instructions:
~~~
conda install pytorch=1.8.1 torchvision=0.9.1 -c pytorch
pip install tensorboard einops scikit-image pytorch_msssim opencv-python
~~~
Install warmup scheduler:
~~~
cd pytorch-gradual-warmup-lr/
python setup.py install
cd ..
~~~
## Training and Evaluation
Please refer to respective directories.
## Results [Download](https://drive.google.com/drive/folders/1bZb9L660t4jL2wAqr23iTg6eyAnCuUBt?usp=sharing)
|Task|Dataset|PSNR|SSIM|
|----|------|-----|----|
|**Motion Deblurring**|GoPro|33.29|0.963|
||HIDE|31.05|0.941|
||RSBlur|34.31|0.872|
||RealBlur-R|35.84|0.952|
|**Image Dehazing**|SOTS-Indoor|42.45|0.997|
||SOTS-Outdoor|40.40|0.997|
||Dense-Haze|17.13|0.65|
||NH-HAZE|20.55|0.81|
||NHR|26.30|0.976|
||Haze4K|34.12|0.99|
|**Image Desnowing**|CSD|38.37|0.99|
||SRRS|32.33|0.98|
||Snow100K|33.76|0.95|
|**Image Deraining**|Average|33.51|0.916|
|**Defocus Deblurring**|DPDD<sub>*single*</sub>|26.22|0.811|


## Citation
~~~
@article{cui2023image,
  title={Image Restoration Via Frequency Selection},
  author={Cui, Yuning and Ren, Wenqi and Cao, Xiaochun and Knoll, Alois},
  journal={IEEE Transactions on Pattern Analysis and Machine Intelligence},
  year={2023},
  publisher={IEEE}
}
~~~

## Contact
Should you have any question, please contact Yuning Cui.
