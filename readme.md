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
7. Then: ```wget https://github.com/Jer8miah/Messy-room/blob/c6811bf06d70f61e3e58b3bbd96704df77c4f91f/nvdli-data/classification/final.pth ```
8. Open JupyterLab from the link in the beginning
9. Password: ```dlinano```
10. Once inside click ```classification``` folder on the left-hand side.
11. Click on the file ```final.ipynb```
12. Run all the cells by pressing ```CONTROL+ENTER```(Windows), ```COMMAND+ENTER```(Mac).
13. Wait for interactive display apper after all cells were executed
14. Clear the text from in the model path box and paste this: ```/nvdli-nano/data/classification/final.pth```
[Imgur](https://imgur.com/f4Ezr9d)
15. Click the ```load model``` button
16. Put your camrea on a clean or dirty part of the room.
17. Click ```evaluate```
18. You will see the slider changing to what it thinks it is.
[View a video explanation here](https://youtu.be/iE-GbLcX5xc)
