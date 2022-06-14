This script was written to plot the contributions of spatially separated signal gain and loss in different regions of an image to the overall image intensity. It was used to generate figures 3B'', 4B, and 4E' in the publication [_Cell cycle and developmental control of cortical excitability in Xenopus laevis_](https://www.biorxiv.org/content/10.1101/2022.02.11.480124v1 "Link to paper on BioRxiv") .

This script was written specifically to investigate the contributions of net F-actin assembly and net F-actin disassembly to the overall complement of F-actin waves in a region. However, in principle it can be used to interactively visualize the contributions of any fluorescent marker to the mean signal in the image over time. To use it, simply enter the full path to a single-channel time lapse image in .tif format, and (if desired) a path to save the resulting plot values. If you are analyzing a particularly long time lapse, it may be helpful to downsample the image initially to accelerate the computation. To do so, simply enter an integer scale factor > 1. When running, this script will open an interactive matplotlib figure with a slider to adjust the number of frames to compare, and another slider to adjust the number of frames to average. If a satisfactory setting is identified, the values from the plot can be saved by clicking the "Save" button.

![Alt Text](https://github.com/zacswider/README_Images/blob/main/assembly_disassembly_use.gif)

The measurements taken are the sum of pixel values that have increased (blue) or decreased (orange) since the time point _n_ frames previous to it. The rate of change will determine the appropriate value for n. If necessary, a rolling average of sequential frames may be applied. 

Dependencies:
 - Numpy
 - Pandas
 - Scikit-image
 - Matplotlib
