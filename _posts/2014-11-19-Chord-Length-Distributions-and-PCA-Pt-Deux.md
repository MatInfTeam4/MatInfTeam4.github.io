---
layout: post

title: Chord Length Distribution and PCA Part Deux
category: blog

author:
  name: Patxi Fernandez-Zelaia
  bio: Domain Expert 
  image: patxi.png

---

## Chip Morphology and Features of Interest

The primary feature we are attempting to capture is ***chord length***. The strategy is to take multiple images at the bottom of each chip roughly in the middle and quantify gradients in the vertical direction.

[![Image](http://matinfteam4.github.io/images/22/chords/general.png)](http://matinfteam4.github.io/images/22/chords/general.png)

The chord length can be determined by 



1. performing segmentation
2. calculating chord lengths based on binary images.


[![Image](http://matinfteam4.github.io/images/22/chords/chordpic.png)](http://matinfteam4.github.io/images/22/chords/chordpic.png)

## Chord Length Distributions

Performing this operating over 9 images and collecting samples the following distributions may be generated. Note that a 5-pixel bin size was utilized for all computation. We have not performed any sensitivity study regarding bin size yet.

[![Image](http://matinfteam4.github.io/images/22/chords/image.png)](http://matinfteam4.github.io/images/22/chords/image.png)

Note that there appears to be a somewhat subtle change to the distribution at the smallest bin size. Also, the further from the bottom of the image you move, the frequency of large chord measurements increases. Both of these trends agree with what we intuitively expect regarding grain size gradients.

## Principal Component Analysis

Generated chord length distributions across all rows of the image were used to generate a PCA representation. The hope is that we can focus on a few principal components only and be able to track their evolution both 

1. spatially (in the vertical direction of the image) 
2. as a function of processing routes

Below are a few select components.

[![Image](http://matinfteam4.github.io/images/22/chords/princecomp_pdf_1.png)](http://matinfteam4.github.io/images/22/chords/princecomp_1.png)

[![Image](http://matinfteam4.github.io/images/22/chords/princecomp_pdf_2.png)](http://matinfteam4.github.io/images/22/chords/princecomp_2.png)

[![Image](http://matinfteam4.github.io/images/22/chords/princecomp_pdf_3.png)](http://matinfteam4.github.io/images/22/chords/princecomp_3.png)

[![Image](http://matinfteam4.github.io/images/22/chords/princecomp_pdf_28.png)](http://matinfteam4.github.io/images/22/chords/princecomp_28.png)

## Update on pdf formulation

Using a different normalization procedure, the following pdf distributions may be developed.

[![Image](http://matinfteam4.github.io/images/22/chords/image2.png)](http://matinfteam4.github.io/images/22/chords/image2.png)
