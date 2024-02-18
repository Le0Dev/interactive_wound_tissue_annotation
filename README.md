# Interactive wound tissue annotation with one-vs-rest superpixel grabcut

This notebook allows you to annotate the different tissues within a wound using a mask and annotation. Each color from the scribble is considered a class. Thus, it is possible to recover the annotated superpixels and carry out a binary segmentation using the GrabCut algorithm from HSV color features. By considering a one-vs-rest approach it is possible to achieve multiclass segmentation. The disadvantage of this approach is that there may remain unclassified superpixels or superpixels classified in several classes. This problem can be corrected by carrying out a second classification of the problematic superpixels from the well-classified superpixels (not yet implemented). The user has the possibility to adjust the granularity of the segmentation with the parameters of the number of superpixels and compactness (SLIC).
To be fixed: too few superpixels risk causing an overlap when two scribbles are found on the same superpixel.
This code works in the case where a single connected component is present on the mask, it does not manage the presence of several wounds or particles at the same time on the mask as input.

![image](https://github.com/Le0Dev/interactive_wound_tissue_annotation/assets/39364891/acf1ba84-c4ab-4f41-a89b-5b3de7a90464)
