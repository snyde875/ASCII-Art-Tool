# Image Art Creator
A basic application programmed as a personal project that'll currently allow you to do 3 things
* Create ASCII Art (Examples given below)
* Convert between image file types (Supported formats given below)
* Average the colors of an image to create a new image (Examples given below)

As of now, these are the only functions the application is capable of executing. The brighten, blur detection, and warp colors currently do nothing when clicked.

## Setting Up
In order to use the application, all you have to do is download the latest release over [here.](www.google.com) 

However, in order to use the convert file format option, you must download ImageMagick and set MAGICK_HOME enviornment variable to the path of ImageMagick. Note that you do not need to download ImageMagick in order to create ASCII art or use any other of the applications functionalities; only the convert file format option requires ImageMagick. An installation of ImageMagick is required because Wand, one of the dependencies of this application, uses ImageMagick as a dependency. Below is a step-by-step, easy-to-follow walkthrough of getting ImageMagick set up.

## Installing ImageMagick
First, you will need to download "ImageMagick-7.0.10-24-Q16-x86-dll.exe" from [here](http://www.imagemagick.org/download/binaries/) and then run the installation. When installing ImageMagick, make sure you install development headers and libraries for C and C++ as shown in the image below. If the version specified above is not available, pick a version that is at least version 7 (so ImageMagick-7.0.10 and up) and that has "Q16-x86" following it. Q8 and x64 will not work. 

![alt text](https://docs.wand-py.org/en/0.4.1/_images/windows-setup.png)

When installing ImageMagick from the installer, make sure you remember the location of where you're saving ImageMagick. Once ImageMagick has been saved to your computer, you will need to navigate to control panel -> system and security -> system -> advanced system settings. Afterwards, select "Enviornment Variables," and then under "System Variables," hit "new." The variable name should be MAGICK_HOME, and for the variable value, hit "browse directory" and then select your download of ImageMagick. Alternatively, you can search "View Advanced System Settings" from the Windows Search bar and select the Enviornment Variables option from there. 

![alt text](https://docs.wand-py.org/en/0.4.1/_images/windows-envvar.png)

Once ImageMagick has been successfully downloaded and the enviornment variable has been set up, you should be able use the convert file format option of the application.

## Creating ASCII Art

## Converting between formats
In order to use this part of the application, an installation of ImageMagick is required. See the section "Installing ImageMagick" for a quick and easy guide for how to do this.

Currently, you can upload and convert between any of these file formats given below:
* png
* jpg
* ppm (P6, binary)
* ppm (P3, ASCII)
* bmp
* pgm

I've given users the option to convert images to a ppm ASCII format because most file type converters online only give the option to convert an image to a compressed binary ppm. In other words, should you open a ppm ASCII image with notepad, for example, all of the image data will be represented in ASCII RGB values. It's my hope that this will be useful to anyone on windows needing to work with ppm images with a magic number of P3. 


## Averaging colors of an image

## Built With
* [Python 3](https://www.python.org/downloads/) - The primary programming language used
* [Pillow](https://pillow.readthedocs.io/en/stable/) - Mainly used for opening, saving, and converting images to and from a numpy array format
* [NumPy](https://numpy.org/) - Used to represent images in array form
* [Colour](https://pypi.org/project/colour/) - Used to create smooth gradients between two colors
* [PyQt5](https://pypi.org/project/PyQt5/) - The GUI framework
* [Wand](https://docs.wand-py.org/en/0.6.2/) - Used to allow conversion to formats not supported by Pillow, such as PPM P3

## Acknowledgements 
After packaging the python files through PyInstaller to create the executable for the application, I ran into an error stating "ImportError: unable to find Qt5Core.dll." After doing some research on how to solve this problem, I ran into a [stack overflow answer](https://stackoverflow.com/questions/56949297/how-to-fix-importerror-unable-to-find-qt5core-dll-on-path-after-pyinstaller-b) that solved my problem. Sofair R. provided a code snippet that I imported into my main python file and the import error was fixed. 

In addition, while programming the ASCII art creator, I used two articles for reference:
* [Convert Photos to ASCII Arts with Python](https://wshanshan.github.io/python/asciiart/)
* [Converting an Image to ASCII Image in Python](https://www.geeksforgeeks.org/converting-image-ascii-image-python/)

The first article is also what gave me the idea to create ASCII art using color gradients. 

I also taught myself how to use PyQt5 using a series of articles hosted [here.](https://www.learnpyqt.com/)

Finally, the k-means algorithm used in the "Group Colors" functionality of the application was originally a class project for my CSCI 1913 Data Structures and Algorithms class taught by Daniel Kluver. I made slight modifications to the original code, such as using python PIL to open images and numpy to represent images, but the algorithm as a whole is largely still the original algorithm used for that class. 
