- Before you take a picture, it is often a good idea to check what the camera sees. To do this you can use the `start_preview()` and `stop_preview()` methods. Before doing this though, you'll need to also import the `sleep` method from the `time` module, so that you can have a pause between the preview opening and closing.

	~~~python
	from picamera import PiCamera
	from time import sleep

	camera = PiCamera()

	camera.start_preview()
	sleep(2)
	camera.stop_preview()
	~~~

- Save and run the code and you should see the view from the PiCamera displayed on the screen.

- You can make the preview slightly transparent. This means if your code crashes, it's easy to find the Python shell and close it, which will kill the preview. To make the preview transparent, you can provide `camera.start_preview()` with an `alpha` value.

	~~~python
	from picamera import PiCamera
	from time import sleep

	camera = PiCamera()

	camera.start_preview(alpha=190)
	sleep(2)
	camera.stop_preview()
	~~~
