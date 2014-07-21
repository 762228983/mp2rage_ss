mp2rage_ss-fs
=============

This scripts is to do skullstripping on T1w image from the MP2RAGE sequence and feed it to FreeSurfer to generate cortical surfaces.

It will use BET/FSL, VBM8/SPM8, and FreeSurfer. So you need to have them executable beforehand.

1. download the "vbm8_brainExt_exit.m" into any working MATLAB path
2. download the "mp2rage_ss-fs" in any working bash path
3. type "mp2rage_ss-fs" without any arguments to see the help message as below:
---
mp2rage_ss-fs runs skullstripping on T1-weighted image obtained with MP2RAGE sequence
using BET/FSL and VBM8/SPM and subsequently feed it into FreeSurfer.

Usage  : mp2rage_ss-fs (options) [subjectID] [T1w_filename] [inv2_filename] [(optional)SUBJECTS_DIR]
(options)
-1     : stops process after skullstripped "ana_brain.nii.gz"
(arguments)
  [subjectID]     : subject ID for FreeSurfer
  [T1w-filename]  : filename of T1-weighted image from MP2RAGE sequence
  [inv2-filename] : filename of the second inversion image from MP2RAGE sequence
  [SUBJECTS_DIR]  : optionally \"subjects\" directory for FreeSurfer can be specified, otherwise it will be the current path by default

Example: mp2rage_ss-fs -1 WN6T mp2rage_uni.nii mp2rage_inv2.nii

NOTE: You need to have FSL and SPM executable and "vbm8_brainExt_exit.m" in your MATLAB working path.

(cc) 2014, sgKIM. solleo@gmail.com
---

