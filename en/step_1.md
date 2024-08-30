#### Preview your photo

- Before you take a picture, it is often a good idea to check what the Camera Module sees. To do this you can use the `start_preview()` and `stop_preview()` methods. 

First though, you'll need to import the `sleep` method from the `time` module, so that you can have a pause between the preview opening and closing.

```python
from picamzero import Camera
from time import sleep

cam = Camera()
cam.start_preview()
sleep(2)
cam.take_photo("test.jpg")
cam.stop_preview()
```

- Save and run the code. You should see the view of the Camera Module displayed on the screen for two seconds, then it will close.

#### Add transparency

- You can make this preview slightly transparent. You'll want to this in case your code crashes - if the preview is transparent, it's easy to find and close the Python shell and thereby kill the preview. 

You'll need to provide the `cam.start_preview()` method with an `alpha` value, which determines the preview's transparency. The lower the number, the more transparent the preview will be.

```python
from picamzero import Camera
from time import sleep

cam = Camera()

cam.start_preview(alpha=190)
sleep(2)
cam.take_photo("test.jpg")
cam.stop_preview()
```

#### Documentation

- [https://raspberrypifoundation.github.io/picamera-zero](https://raspberrypifoundation.github.io/picamera-zero){:target="_blank"}
