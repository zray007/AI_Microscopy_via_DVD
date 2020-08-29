# AI_Microscopy_via_DVD
# Pre-trained model
A pretrained generator model on the DIV2k dataset is provided in the 'models' directory. It uses 6 inverted residual blocks, with 32 filters in every layer of the generator.

Upsampling is done via phase shifts in the low resolution space for speed.

To try out the provided pretrained model on your own images, run the following:
```bash
python infer.py --image_dir 'path/to/your/image/directory' --output_dir 'path/to/save/super/resolution/images'
```
