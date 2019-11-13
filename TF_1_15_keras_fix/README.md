# Singularity_img
Storage of singularity definition file and bug fix for keras MultiGPU processing.


Here is a fast and simple way to run multi_gpu trainig in keras with Tensorflow 1.15 backend the fix for issue like [this](https://github.com/keras-team/keras/issues/13057#issuecomment-520553490) (AttributeError: 'DeviceSpecV1' object has no attribute 'split') is added. Midified device_spec.py with this line:


```
if isinstance(spec, DeviceSpecV1):
      # Capture a snapshot of spec.
      
      spec = spec.to_string()
```


Place both files in one directory and run ```sudo singularity build TF_1_15_fix.sif TF_1_15_keras.def```
 
