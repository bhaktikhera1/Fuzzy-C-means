# Fuzzy-C-means
Type of Intensity Normalization : Fuzzy C Means
# Fuzzy C Means

_intensity_normalization.normalize.fcm_

use fuzzy c-means to find a mask for the white matter given a T1w image and it’s brain mask.  Create a WM maskfrom that T1w image’s FCM WM mask.  Then we can use that WM mask as input to the func again, where the WMmask is used to find an approximate mean of the WM intensity in another target contrast, move it to some standardvalue.

**Author:** Blake Dewey (blake.dewey@jhu.edu),Jacob Reinhold (jacob.reinhold@jhu.edu)
Created on: Apr 24, 2018
intensity_normalization.normalize.fcm.fcm_normalize(img,wm_mask,norm_value=1)
_Use FCM generated mask to normalize the WM of a target image_

**Parameters**

*  **img**(nibabel.nifti1.Nifti1Image) – target MR brain image
*  **wm_mask**(nibabel.nifti1.Nifti1Image) – white matter mask for img
*  **norm_value**(float) – value at which to place the WM mean

**Returns** img with WM mean at norm_value

intensity_normalization.normalize.fcm.**find_wm_mask**(img,brain_mask,threshold=0.8)

_find WM mask using FCM with a membership threshold_

**Return type** normalized (nibabel.nifti1.Nifti1Image)

**Parameters**

* img(nibabel.nifti1.Nifti1Image) – target img
* brain_mask(nibabel.nifti1.Nifti1Image) – brain mask for img
* threshold(float) – membership threshold

**Returns** white matter mask for img

**Return type** wm_mask (nibabel.nifti1.Nifti1Image)


