mp2rage_ss
=============

This scripts is to do skullstripping on T1w image from the MP2RAGE sequence.

0. It will use BET/FSL and VBM8/SPM8. So you need to have them executable beforehand:
```
source ${your_FSL}/fsl.sh
export MATLABPATH=$MATLABPATH:${your_SPM}
```

1. download the "vbm8_brainExt_exit.m" and "mp2rage_ss" into a directory `${your_mp2rage_ss}` or any working path
2. set paths executable:
```
export PATH=$PATH:${your_mp2rage_ss}
export MATLABPATH=$MATLABPATH:${your_mp2rage_ss}
```
3. type "mp2rage_ss-fs" without any arguments to see the help message as below:
```
mp2rage_ss runs skullstripping on T1-weighted image obtained with MP2RAGE sequence using BET/FSL and VBM8/SPM and returning "ana_brain.nii.gz" as the final result.

Usage  : mp2rage_ss [T1w_filename] [inv2_filename]
(arguments)
  [subjectID]     : subject ID for FreeSurfer
  [T1w-filename]  : filename of T1-weighted image from MP2RAGE sequence
  [inv2-filename] : filename of the second inversion image from MP2RAGE sequence

Example: mp2rage_ss mp2rage_uni.nii mp2rage_inv2.nii

NOTE: You need to have FSL and SPM executable and "vbm8_brainExt_exit.m" in your MATLAB working path.

(cc) 2014, sgKIM. solleo@gmail.com
```

