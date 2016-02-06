# Simple Image Crop App
Unfortunately not all Android devices are shipped with an app able to crop images based on an intent. 
The [android-crop project](https://github.com/jdamcd/android-crop) provides an activity to crop images 
but does not specify an appropriate intent filter. Hence, this project is basically a just a wrapper
which defines an intent filter for the crop activity of the [android-crop project](https://github.com/jdamcd/android-crop).
The app does not define a launcher activity. Thus, it can only be used if it is started with the correct intent.

## Intent Details
* Action: de.dwolt.imagecrop.action.CROP
* Data: URI pointing to the image which should be cropped
* Extra "max_x": Maximum width of the cropped image
* Extra "max_y": Maximum height of the cropped image
* Extra "aspect_x": If the cropped image should have a ratio of X:Y, this extra is used to define the x part of the ratio.
* Extra "aspect_y": If the cropped image should have a ratio of X:Y, this extra is used to define the y part of the ratio.
* Extra "output": URI defining where the cropped image should be saved

## Known Issues
On some device the orientation of the cropped image is wrong. However, this is an issue of the [android-crop project](https://github.com/jdamcd/android-crop).
