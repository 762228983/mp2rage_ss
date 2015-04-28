mp2rage_ss
=============
runs skullstripping on MP2RAGE images with the uniform tissue contrast image (uni_fname)  and the 2nd inversion image (inv2_fname) by

[1] multiplying uni and inv2

[2] and using skull-stripping using VBM8/SPM

and returns skull-stripped image (uni_fname+"_mp2brain.nii" by default)
````
Usage  : ${myname} [uni_filename] [inv2_filename] ([output_filename])
(arguments)
  [uni-filename]  : filename of uniform contrast image from MP2RAGE sequence
  [inv2-filename] : filename of the second inversion image from MP2RAGE sequence
  [output]        : (optional) output filename
````
Reference: Fujimoto et al, 2014, NeuroImage. 

Example: mp2rage_ss mp2rage_uni.nii mp2rage_inv2.nii

NOTE: You need to have SPM executable and "vbm8_brainExt_exit.m" in your MATLAB working path.

(cc) 2015, sgKIM. solleo@gmail.com
