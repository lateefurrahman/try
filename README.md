# try
import picture 
Updates about the image to numpy assignments

​

you need to download 20 photos and save in the photos folder

use the following codes to scan the folder (change folder name from '.' to photos

# Import the os module, for the os.walk function

import os

# Set the directory you want to start from

rootDir = '.'

for dirName, subdirList, fileList in os.walk(rootDir):

print('Found directory: %s' % dirName)

for fname in fileList:

print('\t%s' % fname)

print('Found directory: %s' % dirName)to for fname in fileList:e name (with input) as input and load it and

resize it to 200, 200, 3  and return a numpy array. you need an image resize library like PIL

​

4) store this numpy array of the image into the main array (created earlier in the code with 20, 200, 200, 3 dimensions 

​

Note: you can find some partial code in this group

​

a = ("photos folder")

print(a)

photos folder

from PIL import Image

import numpy as np

a = Image.open("lateef.jpg")

a = np.array(img)

from PIL import Image

ap = Image.open("lateef.jpg")

ap.rotate(45).show()

ap

a

a.astype

<function ndarray.astype>

a.clip

<function ndarray.clip>

a.compress

<function ndarray.compress>

a.imag

array([[[0, 0, 0],
        [0, 0, 0],
        [0, 0, 0],
        ...,
        [0, 0, 0],
        [0, 0, 0],
        [0, 0, 0]],

       [[0, 0, 0],
        [0, 0, 0],
        [0, 0, 0],
        ...,
        [0, 0, 0],
        [0, 0, 0],
        [0, 0, 0]],

       [[0, 0, 0],
        [0, 0, 0],
        [0, 0, 0],
        ...,
        [0, 0, 0],
        [0, 0, 0],
        [0, 0, 0]],

       ...,

       [[0, 0, 0],
        [0, 0, 0],
        [0, 0, 0],
        ...,
        [0, 0, 0],
        [0, 0, 0],
        [0, 0, 0]],

       [[0, 0, 0],
        [0, 0, 0],
        [0, 0, 0],
        ...,
        [0, 0, 0],
        [0, 0, 0],
        [0, 0, 0]],

       [[0, 0, 0],
        [0, 0, 0],
        [0, 0, 0],
        ...,
        [0, 0, 0],
        [0, 0, 0],
        [0, 0, 0]]], dtype=uint8)

a.T.shape

(3, 720, 720)

a

a.resize((2,20))

---------------------------------------------------------------------------
ValueError                                Traceback (most recent call last)
<ipython-input-106-21277b726415> in <module>
----> 1 a.resize((2,20))

ValueError: cannot resize an array that references or is referenced
by another array in this way.
Use the np.resize function or refcheck=False

a.reshape(30,-1)

array([[ 22,   9,   0, ..., 150, 117,  74],
       [186, 141,  99, ..., 142, 111,  80],
       [193, 151, 113, ...,  85,  58,  37],
       ...,
       [167, 127,  91, ..., 140, 125, 106],
       [164, 122,  84, ..., 137, 119,  99],
       [190, 148, 108, ..., 152, 132, 121]], dtype=uint8)

a

from PIL import Image

import glob, os

​

size = 8000, 9000

​

​

for infile in glob.glob("lateef.jpg"):

    file, ext = os.path.splitext(infile)

    a = Image.open(infile)

    a.thumbnail(size)

    #im.save(file + "JPEG"

a

a.array

---------------------------------------------------------------------------
AttributeError                            Traceback (most recent call last)
<ipython-input-108-2896a26f1581> in <module>
----> 1 a.array

AttributeError: 'numpy.ndarray' object has no attribute 'array'

a

from PIL import Image

import numpy as np

arr = Image.open("lateef.jpg")

arr = np.array(img)

arr

array([[[ 22,   9,   0],
        [ 22,   9,   0],
        [ 23,  10,   0],
        ...,
        [106,  86,  49],
        [ 75,  57,  21],
        [ 42,  26,   0]],

       [[ 58,  41,  23],
        [ 59,  42,  24],
        [ 60,  43,  25],
        ...,
        [145, 125,  88],
        [106,  88,  52],
        [ 67,  48,  15]],

       [[124,  98,  73],
        [126, 100,  75],
        [128, 102,  77],
        ...,
        [180, 158, 121],
        [128, 108,  73],
        [ 77,  59,  23]],

       ...,

       [[199, 161, 122],
        [197, 159, 120],
        [195, 157, 118],
        ...,
        [226, 202, 178],
        [192, 169, 153],
        [160, 138, 125]],

       [[201, 163, 124],
        [201, 163, 124],
        [202, 164, 125],
        ...,
        [227, 205, 182],
        [194, 173, 156],
        [163, 141, 130]],

       [[195, 157, 118],
        [198, 160, 121],
        [202, 164, 125],
        ...,
        [220, 198, 175],
        [186, 164, 150],
        [152, 132, 121]]], dtype=uint8)

arr[0]

array([[ 22,   9,   0],
       [ 22,   9,   0],
       [ 23,  10,   0],
       ...,
       [106,  86,  49],
       [ 75,  57,  21],
       [ 42,  26,   0]], dtype=uint8)

arr[0] = 786

arr

array([[[ 18,  18,  18],
        [ 18,  18,  18],
        [ 18,  18,  18],
        ...,
        [ 18,  18,  18],
        [ 18,  18,  18],
        [ 18,  18,  18]],

       [[ 58,  41,  23],
        [ 59,  42,  24],
        [ 60,  43,  25],
        ...,
        [145, 125,  88],
        [106,  88,  52],
        [ 67,  48,  15]],

       [[124,  98,  73],
        [126, 100,  75],
        [128, 102,  77],
        ...,
        [180, 158, 121],
        [128, 108,  73],
        [ 77,  59,  23]],

       ...,

       [[199, 161, 122],
        [197, 159, 120],
        [195, 157, 118],
        ...,
        [226, 202, 178],
        [192, 169, 153],
        [160, 138, 125]],

       [[201, 163, 124],
        [201, 163, 124],
        [202, 164, 125],
        ...,
        [227, 205, 182],
        [194, 173, 156],
        [163, 141, 130]],

       [[195, 157, 118],
        [198, 160, 121],
        [202, 164, 125],
        ...,
        [220, 198, 175],
        [186, 164, 150],
        [152, 132, 121]]], dtype=uint8)
