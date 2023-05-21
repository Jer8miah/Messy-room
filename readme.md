# Messy Room

This AI was created to determine when your room is getting messy or if it's still clean.

![add image descrition here](direct image link here)

## The Algorithm
To differentiate between a clean and a dirty room, my program uses image detection. The USBCAMERA and CSICAMERA libraries from jetcam are imported into the code to make it function. It first checks to see if you're using a CSI or USB camera before turning on the camera. Then it decides which categories, such as Clean and Dirty, it wants to collect data from. The following lines of code are then executed:
```import ipywidgets import traitlets from IPython.display import display from jetcam.utils import bgr8_to_jpeg```
It then begins categorizing the pictures. The model is trained using ```Torch``` and ```TorchVision``` and my own network is built on top of Resnet-18. The classifier receives a live video stream, which I use to judge wheter it is clean.

## Running this project

1. ssh into your nano
2. Type: ```./docker_dli_run.sh```
3. Once in the docker, type: ```cd classification```
4. Then: ```wget https://github.com/Jer8miah/Messy-room/blob/5bc2a5e55dd28aaa6e3dc7a83e0bb4a4f679fdf5/Final.ipynb``` 
5. Type: ```cd``` to navigate back to your home directory in the docker
6. Then: ```cd data/classification``` 
7. 

[View a video explanation here](video link)
