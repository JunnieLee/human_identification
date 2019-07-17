# human_identification


: [ Image Retrieval with Color Coherence Vectors ]
   
--------------------------------------------------------------------------------------------

* Some online posts to refer to :


1) https://owlcation.com/stem/Image-Retrieval-Color-Coherence-Vector


Global / Local Color Histograms have some clear issues, for example GCH doesn't encode any information about the color spatial distribution in the image. LCH performs much better than GCH as it overcomes this specific problem to some extent, but it is still not robust enough to some little variations like image rotations and flips.

So, we’ll discuss a more useful yet fast color descriptor that is capable of encoding information about color spatial distribution which is called Color Coherence Vector (CCV).  It works by classifying each pixel as either coherent or incoherent. Coherent pixel means that it is part of a big connected component (CC) while incoherent pixel means that it is part of a small connected component. A crucial step for this method to work is defining the criteria by which we decide whether a connected component is big or not.

(+ explains further algorithms)

(기본개념 이해하는데에 제일 좋은 링크)



2)




3)


--------------------------------------------------------------------------------------------

* Papers to refer to :

1)
( Image Similarity Measure using Color Histogram, Color Coherence Vector, and Sobel Method : https://pdfs.semanticscholar.org/b539/791e55d550b493701c82f76c4867b3b88a3a.pdf )


There exist many CBIR systems, which retrieve images by
color histogram. But only histogram based method cannot
give best results if two pictures have same color distribution.
For this reason we Consider Color Coherence Vector also as
a color feature extraction method. We define a color's
coherence as the degree to which pixels of that color are
members of large similarly-colored regions. We refer to
these significant regions as coherent regions, and observe
that they are of significant importance in characterizing 
images. Our coherence vector classifies image pixels as
either coherent or incoherent in type. Coherent pixels are a
part of some sizable contiguous region, while incoherent
pixels are not. A coherent pixel is part of a large group of
pixels of the same color, while an incoherent pixel is not. We
determine the pixel groups by computing connected
components. In this method some region is created based on
color information. Details Method to extract color coherence
vector is described in the section-Proposed method. 




Step 1: Read the image.


Step 2: Calculate the size of the image


Step 3: Compute 4 different array from original array which
is created after reading the image. In the first array, 1st row
value of the original image will be stored as last row. In
second array, last row value of the original image will be
stored as first row. In the next two array column value of the
original image will be replaced in this manner. 


Step 4: Convert the entire 5 image array into double data
class in MATLAB.


Step 5: Take the average of 5 image array.


Step 6: Then make a matrix which is combination of Red,
Green, Blue, (Red +Green), (Red +Blue), (Blue +Green),
White and Black value of an image and they are initializes as
default value.


Step 7: Now we measure the magnitude of difference from
the average matrix which is get in Step5 and the value said in
step6 for each 8 distinct element.


Step 8: Then we calculate the threshold value which will
give best result.


Step 9: Using the threshold value calculate how many Red
channel connected pixel we get and we called it as a Red
Coherent(Re), and find also how many pixel do not contain
any red information and we called it as a Red incoherent(Ri).
We continue this process for all 8 different color information
said in step6.


Step 10: Finally we get 16 different Coherent and Incoherent
value from the image and store it in a previously created
array.


Step 11: Repeat step 1 to 10 for every image in the database. 







2)

3)

4)

5)

6)

7)

8)


--------------------------------------------------------------------------------------------

* Github projects to refer to :


1) https://github.com/TarekVito/ColorCoherenceVector 

  : can checkout some ideas but it's written in matlab language



2) https://github.com/krinnewitz/ccv

   : written in C++



[ *** WRITTEN IN PYTHON *** ] // best code reference


3) https://bitbucket.org/aihara/pyccv/src/default/


4) stack blur
http://www.quasimondo.com/StackBlurForCanvas/StackBlurDemo.html 



// -> 3) & 4) mashed up :  https://github.com/buhii/ccv.js



[ *** WRITTEN IN PYTHON *** ] (simple ver_)

5) https://github.com/tamanobi/ccv/blob/master/ccv.py



[ *** WRITTEN IN PYTHON *** ] // the second best code reference
6) https://github.com/kohjingyu/color-coherence-vectors



