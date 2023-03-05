# coinClassification
Localise and classify coins in an image and visualise the results.

Functions/scripts written by Eleni Christoforidou in MATLAB R2022b.

The coinClassification script localises and classifies coins in an image, and allows visualisation of the resutls.

The following helper functions are used in the script:

MakeCircleMatchingFilter: This function takes as input the diameter for the circle as well as W, the filter size for the matching filter. It outputs the [WxW] matrix filter, which is a binary mask that contains, as foreground, a circle with width diameter centered in the matrix surrounded by background pixels. The variable filter serves as a matching filter for circular shapes with approximately the same diameter. The function also outputs xc and yc,  the coordinates of the center of the filter, as 2nd and 3rd optional outputs.

AddCoinToPlotAndCount: This function takes as input x and y, coordinates for the centroid of a coin found in the image, cls, its classification label indicating whether it was found to be a dime, nickel, or quarter. The function outputs coinvalue, the value (in cents) of the coin that was found. It also plots, in the current figure, a circle centered at x and y with radius and color unique for each coin type according to the table below. The function also has 2nd and 3rd outputs x_plot and y_plot, the list of x and y coordinates of the vertices of the circle being plotted. The function also has a 4th output col, the color string of the circle plotted.

OtsuThreshold: This function takes as input an [MxN] uint8 image matrix img, and outputs the Otsu thresholded binary image in [MxN] matrix msk, as well as the integer threshold thrsh used to make msk.
