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



