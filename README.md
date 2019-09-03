# SurvivalAnalysis
A collection of R commands for typical epidemiological analyses and publication-ready output. Functions for repeated regression, test-for-trend in proportions, and more are located within. A series of Excel functions to simplify retrospective (or prospective) survival analysis is also provided.

## The Problems and Solutions
### Converting adverse event date collections into interpretable survival data
Imagine the following: you have a massive excel file with hundreds of rows of patients. Tens of columns of event types. And a bunch of dates for when each date occurs, if at all. When conducting survival analysis, either Cox regression or Kaplan Meier, you need processed data. You need just survival time, and survival status. But how can you reconcile all the different event types together, in a way that allows you to easily experiment with which adverse events should be included in the model?

<img src="https://github.com/malyalar/SurvivalAnalysis/blob/master/excelFunctions/Excel%20screenshot.png">

The function provided within allows you to eaily input (with a 0 or 1) which adverse events should be included in the survival model, and then generate survival data. Furthermore, it can differentiate between events that occurred BEFORE a certain date, or AFTER a certain date. In this case, adverse event data was collected, but not all adverse events occurred AFTER the date of transplant. The function provided will allow you to differentiate, and count only post-transplant events. 

<img src="https://github.com/malyalar/SurvivalAnalysis/blob/master/excelFunctions/Solution%20screenshot.png">


### Converting survival functions into publication-ready output
While current ggtheme outputs generate beautfiful color graphs, few journals accept color figures without an extra charge to the author. Here are some ggtheme parameters that probably generate the style of figure that most epidemiology journals are looking for. Included underneath are the requisite risk and cumulative events tables that many journals look for as well.
<p>
<img src="https://github.com/malyalar/SurvivalAnalysis/blob/master/excelFunctions/Time%20to%20MACE%2C%20RWT%20diagnosis.png" width=400>
<img src="https://github.com/malyalar/SurvivalAnalysis/blob/master/excelFunctions/Time%20to%20MACE%2C%20LVH%20type.png" width=400>  
</p>
