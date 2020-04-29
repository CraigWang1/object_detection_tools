# Script Guide

## COCO_format.py
This is a script to take a directory with images and corresponding xml labels in pascal (labelImg) format, and format it into COCO format. This is useful for taking custom datasets and training machine learning models on them. The script can also resize the images.

```
usage: COCO_format.py [-h] [--image_dir IMAGE_DIR] [--annot_dir ANNOT_DIR]
                      [--save_dir SAVE_DIR] [--ext EXT]
                      [--target_size TARGET_SIZE] [--one_side ONE_SIDE]
                      [--train_test_split TRAIN_TEST_SPLIT]

Put dataset in COCO format for machine learning training.

optional arguments:
  -h, --help            show this help message and exit
  --image_dir IMAGE_DIR
                        Directory path to dataset images.
  --annot_dir ANNOT_DIR
                        Directory to image annotations.
  --save_dir SAVE_DIR   Directory path to save entire COCO formatted dataset.
                        (eg: /home/user)
  --ext EXT             Image files extension (ex. jpg, png, etc.).
  --target_size TARGET_SIZE
                        Target size to resize as a tuple of 2 integers.
  --one_side ONE_SIDE   Side (int value) to resize image (eg. 512, 1024x556 =>
                        512x278).
  --train_test_split TRAIN_TEST_SPLIT
                        Portion of images used for training expressed as a
                        decimal (eg. 0.90
```
A note to make is that the `target_size` parameter is for resizing to a specific size that is specified (eg. "(420,69)"), while `one_side` resizing is to resize one side of the image to be the specified side (eg. 420), and the other side goes with it. One_side resizing preserves the aspect ratio, and you only specify the integer side length (eg. 512).


