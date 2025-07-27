<samp>
    
# Real-time-Vehicle-Dection-Python

This repository consist of a source code of script to detect cars in a video/camera frame and then draw rectangaluar boxes around them.

The **ML algorithms** used for detecting cars and bounding boxes coordinates is a pretrained cascade model [Haarcascade car](https://github.com/Michelle0303/Real-time-vehicle-dection-/blob/master/haarcascade_car.xml).

## Getting started

First clone the project repository or download the zip of project and then extract it.

```bash
git clone https://github.com/Michelle0303/Real-time-Vehicle-Dection-Python
cd Real-time-Vehicle-Dection-Python
Real-time-Vehicle-Dection-Python ->
```

## Dependencies

Now once you have the project repo in your local directory, install the dependecies required to run the script

```bash
pip install opencv-python
```

## Sample video

The sample video used in this project is [**cars.mp4**](https://github.com/Michelle0303/Real-time-vehicle-dection/blob/master/cars.mp4) which will come as you download or clone the repository, to load a different video with different filename, you might want to change the source code.

```python
def Simulator():
    CarVideo = cv2.VideoCapture('cars.mp4') # change cars.mp4 to name of your vidoe
    while CarVideo.isOpened():
        ret, frame = CarVideo.read()
        controlkey = cv2.waitKey(1)
        if ret:        
            cars_frame = detect_cars(frame)
            cv2.imshow('frame', cars_frame)
        else:
            break
        if controlkey == ord('q'):
            break

    CarVideo.release()
    cv2.destroyAllWindows()

```

## Running the script**

Now you can launch your scripts;

```bash
python app.py 
```




