# Singularity_img
Storage of singularity definition file and bug fix for keras.

Here is a fast and simple way to run multi_gpu trainig in keras with Tensorflow 1.12 backend the fix for this [issue](https://github.com/tensorflow/tensorflow/pull/23197) (AttributeError: 'DeviceSpec' object has no attribute 'split') is added. Place both files in one directory and run ```sudo singularity build TF_1_12_fix.sif TF_1_12_keras_fix.def```
 
