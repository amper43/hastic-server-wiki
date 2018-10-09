Use `Peak Model` for detecting peaks or anomalies in your timeseries.

# Workflow

Supposing you have any technic device to which voltage is applied. If you have some dataset with indicator of this voltage, you can track all peaks, that arrised for a period of time, identify the necessary, filter out the wrong patterns.

# Definition

Firstly, it would be nice to understand what a peak is.
The peak is a sharp increase in the data value with the subsequent return to the original value, the maximum value of the data at the peak is exactly one.

For example, peak it is:

:some picture:

And this is the peak:

:some picture:

And this one:

:some picture:

But this is not the peak!

:some picture:

This is certainly not the peak:

:some picture:

nope:

:some picture: 


# Analytics

Suppose you have already uploaded your dataset and want to analyze it. In the tab choose something and  do something else.
In the section with models, select the peaks. Next, select the zone that approachs for your understanding of the peak, and better choose a few for improving learning quality and reduce scatter. Generally, one leabled peak is enough for working training.

:some picture:

On selected patterns analyst will learn, find all possible peaks and compare them with the originally selected and filter wrong peaks. As a result of the analysis:

:some picture:

For example, you need only one kind of peaks, and the spread needs to be reduced, so you label a few of "wrong" peaks as `delete` peak and run learnig again. Now check boundaries decreased and patterns coinciding with deleted peaks will be filtered out. In the result you will see:

:sad picture, because deletion doesn't working:

# Resume

