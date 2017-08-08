- Before you take a picture, it is often a good idea to check what the Camera Module sees. To do this you can use the `start_preview()` and `stop_preview()` methods. First though, you'll need to import the `sleep` method from the `time` module, so that you can have a pause between the preview opening and closing.

	~~~python
	from picamera import PiCamera
	from time import sleep

	camera = PiCamera()

	camera.start_preview()
	sleep(2)
	camera.stop_preview()
    camera.close()
	~~~

- Save and run the code. You should see the view of the Camera Module displayed on the screen.

- You can make this preview slightly transparent. You'll want to this in case your code crashes - if the preview is transparent, it's easy to find and close the Python shell and thereby kill the preview. You'll need to provide the `camera.start_preview()` method with an `alpha` value, which determines the preview's transparency.

	~~~python
	from picamera import PiCamera
	from time import sleep

	camera = PiCamera()

	camera.start_preview(alpha=190)
	sleep(2)
	camera.stop_preview()
    camera.close()
	~~~
