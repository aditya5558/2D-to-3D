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
| Deep-3D       | 0.22408 | 0.25312 |
| Deep-3D Early Fusion      | 0.1148     | 0.0499 |
| Deep-3D Late Fusion  |  0.1094     |  0.0463 |
