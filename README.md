# Camera Trap

## Install

Check that the camera exists: `libcamera-hello --list-cameras -n -v`.

Take a test photo: `libcamera-still --width 1920 --height 1080 -o test.jpg -n -t 1` (experiment with params, this might be slow!)

For *Raspberry Pi Zero 2 W*:

Add camera information to `/boot/config.txt`. For instance, add the line `dtoverlay=imx219` for the Pi 2 camera. [More camera info here](https://www.raspberrypi.com/documentation/accessories/camera.html#getting-started).

Add legacy camera support: `sudo raspi-config` > Inferface Settings.

Probably change timeout: add the line `camera_timeout_value_ms": 10000` to the file `/usr/share/libcamera/pipeline/rpi/vc4/rpi_apps.yaml`.



`sudo apt-get install python3-opencv`

