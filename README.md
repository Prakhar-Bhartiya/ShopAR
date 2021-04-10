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
we are using smplx and OpenPose for fitting the clothes to a virtual mannequin of the user that is obtained from a single image(monocular) of a mobile camera.

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


### Visualizing Results

Visualizing the result from Zappar where the 3d model is augmented in the real world

## Dependencies

Follow the installation instructions for each of the following before using the
fitting code.

1. [PyTorch](https://pytorch.org/)
2. [SMPL-X](https://github.com/vchoutas/smplx)
3. ZAPPAR (For Augmented Reality)
4. Blender (For cloth Stitching)
5. OpenPose for human detection and pose detection
