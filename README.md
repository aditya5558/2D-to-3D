# 2D-to-3D
11785 Deep Learning Course Project


To access driving stereo data (unpacked size will be 77GB):
- Open an AWS instance
- aws s3 cp s3://idl-proj-3d/driving_stereo.tar.gz ./
- tar -xvzf driving_stereo.tar.gz

(note: do not download this from S3 to outside of AWS, as that will incur huge data egress costs)

This contains a 'train' directory with 174,437 image pairs and 'test' directory with 7,751 image pairs.

Both 'train' and 'test' have 'left' and 'right' folder which contain the images. Thus the 'train' or 'test' directory paths can be passed to the "class Inria(data.Dataset)".

## Results

### Dataset: Inria

| Model        | Train MAE     | Test MAE|
| ------------- |---------------| ------|
| Deep-3D       | 6.36 | 7.58 |
| Deep-3D + Monocular Depth Estimation + Mask-RCNN (Early Fusion)      | 6.50     | 7.29 |
| Deep-3D + Monocular Depth Estimation + Mask-RCNN (Late Fusion)  | 6.31     |  6.84 |


## Example Inputs and Outputs as GIFs
![Image 0 GIF](output_gifs/0.gif)
![Image 1 GIF](output_gifs/1.gif)
![Image 2 GIF](output_gifs/2.gif)
![Image 3 GIF](output_gifs/3.gif)
![Image 4 GIF](output_gifs/4.gif)
![Image 5 GIF](output_gifs/5.gif)
![Image 6 GIF](output_gifs/6.gif)
