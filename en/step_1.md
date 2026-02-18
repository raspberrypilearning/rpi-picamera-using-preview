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


#### Documentation

- [https://raspberrypifoundation.github.io/picamzero](https://raspberrypifoundation.github.io/picamzero){:target="_blank"}
