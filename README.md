# 2D-to-3D
11785 Deep Learning Course Project


To access driving stereo data (unpacked size will be 77GB):
- Open an AWS instance
- aws s3 cp s3://idl-proj-3d/driving_stereo.tar.gz ./
- tar -xvzf driving_stereo.tar.gz

This contains a 'train' directory with 174,437 image pairs and 'test' directory with 7,751 image pairs.

Both 'train' and 'test' have 'left' and 'right' folder which contain the images. Thus the 'train' or 'test' directory paths can be passed to the "class Inria(data.Dataset)".
