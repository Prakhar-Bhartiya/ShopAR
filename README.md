## ShopAR

## Table of Contents
  * [Description](#description)
    * [Fitting](#fitting)
    * [Different Body Models](#different-body-models)
    * [Visualizing Results](#visualizing-results)
  * [Dependencies](#dependencies)


## Description
Shopping online for clothes and accessories is made more personal, by letting the Shoppers/Users try on the clothes visually. before actually ordering them. We use Augmented Reality technology on a users mobile browser so that , they don't actually have to download another app. Our product can work as a webpage. The user can click only one single image for personalising his mannequin to their size. Hence they can now easily try on the clothes with different color and size to see which fits the best and which design matches their personality well

### Fitting
we are using SMPLX[https://github.com/vchoutas/smplify-x] and OpenPose[https://github.com/CMU-Perceptual-Computing-Lab/openpose] for generating a custom 3D Human model for each users (virtual mannequin) from a single image(monocular) of a mobile camera.

### Different Body Models

To fit [SMPL](http://smpl.is.tue.mpg.de/) or [SMPL+H](http://mano.is.tue.mpg.de), replace the *yaml* configuration file
with either *fit_smpl.yaml* or *fit_smplx.yaml*, i.e.:
 * for SMPL:
 ```Shell
 python smplifyx/main.py --config cfg_files/fit_smpl.yaml
    --data_folder DATA_FOLDER
    --output_folder OUTPUT_FOLDER
    --visualize="True/False"
    --model_folder MODEL_FOLDER

 ```
Follow the necessary steps to setup in given dependencies.

### Visualizing Results

Visualizing the result from ZapparWorks[https://zap.works] {WebAR using three.js} where the 3d model is augmented in the real world with feature available [World Tracking/ Image trigger]

## Dependencies

Follow the installation instructions for each of the following before using the
fitting code.

1. [PyTorch](https://pytorch.org/)
2. [SMPL-X](https://github.com/vchoutas/smplx)
3. ZAPWORKS (For Augmented Reality)
4. Blender (For cloth Stitching)
5. OpenPose for human detection and pose detection
