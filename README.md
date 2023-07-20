# License-Plate-Recognition

This image recognition AI recognizes if your car has a license plate.

## The Algorithm

Introducing License Plate Recognizer. Licnese Plate Recognizer uses images of cars with license plate and cars with no licnese plate and recognizes which car has a license plate and which car doesn't. How does it work? The set of training images is used for transfer learning, the val images are used to evaluate the classification's accuracy when it is training the images, and you use the test images after it is done training.

## Steps To Run The Project

1. Make sure you have a Jetson Nano, and install jetson-inference and python3 libaries on your device.
2. Download the 'test', 'train', and 'val' folders, then add these folders to a new folder called 'license_plate' in the models directory at jetson-inference/python/training/classification/data/.
3. Move 'model_best.pth.tar' and 'resnet18.onnx' files to jetson-inference/python/training/classification/models/license_plate directory.
4. Run ```NET=models/license_plate``` and ```DATASET=data/license_plate``` in the Terminal
5. When your done, ```run imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/test/license_plate/Cars2.jpg Cartest0.jpg```
6. If you want to try with your own image, what you'll want to is run the 5th step again, however, replace the image path and the dataset file path with your own image file.


[View a video explanation here](video link)
