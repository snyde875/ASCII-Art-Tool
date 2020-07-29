# Image Art Creator
A basic application programmed as a personal project that'll currently allow you to do 3 things
* Create ASCII Art (Examples given below)
* Convert between image file types (Supported formats given below)
* Average the colors of an image to create a new image (Examples given below)

## Creating ASCII Art

## Converting between formats

## Averaging colors of an image

## Built With
* [Python 3](https://www.python.org/downloads/) - The primary programming language used
* [Pillow](https://pillow.readthedocs.io/en/stable/) - Mainly used for opening and saving images
* [NumPy](https://numpy.org/) - Used to represent images in array form
* [PyQt5](https://pypi.org/project/PyQt5/) - The GUI framework
* [Wand](https://docs.wand-py.org/en/0.6.2/) - Used to allow conversion to formats not supported by Pillow

## Acknowledgements 
After packaging the python files through PyInstaller to create the executable for the application, I ran into an error stating "ImportError: unable to find Qt5Core.dll." After doing some research on how to solve this problem, I ran into a [stack overflow answer](https://stackoverflow.com/questions/56949297/how-to-fix-importerror-unable-to-find-qt5core-dll-on-path-after-pyinstaller-b) that solved my problem. Sofair R. provided a code snippet that I imported into my main python file and the import error was fixed. 

In addition, while programming the ASCII art creator, I used two articles for reference:
* [Convert Photos to ASCII Arts with Python](https://wshanshan.github.io/python/asciiart/)
* [Converting an Image to ASCII Image in Python](https://www.geeksforgeeks.org/converting-image-ascii-image-python/)

The first article is also what gave me the idea to create ASCII art using color gradients. 

I also taught myself how to use PyQt5 using a series of articles hosted [here.](https://www.learnpyqt.com/)

Finally, the k-means algorithm used in the "Group Colors" functionality of the application was originally a class project for my CSCI 1913 Data Structures and Algorithms class taught by Daniel Kluver. I made slight modifications to the original code, such as using python PIL to open images and numpy to represent images, but the algorithm as a whole is largely still the original algorithm used for that class. 
