# Images on the Website

The website requires images to be perfectly square, otherwise the images will get weirdly distorted when displayed with the circular frame. To achieve this required 1:1 aspect ratio, we'll use the open source tool GIMP, and a few simple steps.

## Changing the aspect ratio
Go to https://www.gimp.org and follow the installation instructions appropriate to your system.

### Open
Open the image you want to edit in GIMP, and you'll be presented with a picture that looks like this...

![Gimp Window](https://github.com/novakgroupoxford/bicycle-hugo/blob/master/documentation/img1.png)

### Select
At the top of the main window, you'll see the filename of the image, some information on color profiles and layers, and the current image dimenstions (400 x 451 px in this case). We'll now choose the **Rectangle Select Tool** (top-left in the Toolbox Window), and choose **Fixed Aspect Ratio" in the tool options. This will restrict the aspect ratio of the selection tool to 1:1. You can now select a square region of the image.

![Gimp Rectangle Select](https://github.com/novakgroupoxford/bicycle-hugo/blob/master/documentation/img2.png)

### Crop
After selecting a square region go to the **Image** menu and select **Crop image to selection**

![Gimp Crop Image](https://github.com/novakgroupoxford/bicycle-hugo/blob/master/documentation/img3.png)

### Save
To save your changes, go to **File** and choose **Overwrite [Imagename]**. Alternatively, you can export the edited image as a png file.

![Gimp Save](https://github.com/novakgroupoxford/bicycle-hugo/blob/master/documentation/img4.png)

# Adding an image to a page

To make sure that the system finds the image you want to display, make sure to check the following points:

- The filename in the markdown file matches the filename of the image (e.g. `some_image.jpg` vs. `someimage.jpg`)
- The fileextension in the markdown file matches the fileextension of the image (e.g. `*.jpg` vs `*.JPG` or `*.jpg` vs. `*.png`). Beware: It's case-sensistive!
- The image sits in the appropriate folder: If your markdown file sits in the folder `content/publication`, the system expects to find the image in the folder `static/img/publication`
