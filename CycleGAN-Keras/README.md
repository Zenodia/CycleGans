# Acknowledgement of the original git repo : https://github.com/simontomaskarlsson/CycleGAN-Keras
## Keras implementation of CycleGAN
Implementation using a tensorflow backend. Testing and evaluation done on
street view images. The following gif shows an example of the training
progression in a translation from day to night.

**Left:** Input image. **Middle:** Translated images. **Right:** Reconstructed images.
<img src="./generate_images/synthetic_images/tmp.png" alt="drawing" width="455px"/>

### Model additions as training options
* Identity learning (on different modulus of training iterations)
* PatchGAN in discriminators
* Multi-scale discriminators
* Resize convolution in generators
* Supervised learning with training weight
* Data generator (if using a large dataset)
* Weight on discriminator training labels on real images

---

### Code usage  
1. Prepare your dataset under the directory 'data' and set dataset name to
parameter 'image_folder' in CycleGAN init function.
  * Directory structure on new dataset needed for training and testing:
    * data/Dataset-name/trainA
    * data/Dataset-name/trainB
    * data/Dataset-name/testA
    * data/Dataset-name/testB  

2. Set wanted training options, also found in the init function.

3. Train a model by:
```
python model.py
```



