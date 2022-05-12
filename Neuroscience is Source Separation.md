# Neural Time series Analysis - MX Cohen

## Neuroscience is Source Separation
All mental process are happening together. Signal multiple sourcesso the goal is to separate the multiple sources.

## How can source be separated?
-Anatomical Source Separation : based on anatomy,just study one part of the brain based on anatomy

-Cognititve Source Separation : clever experiment to isolate a single cognitive source like short term mempory

-Temporal Source Separation :

-Spatial Source Separation :

-Statical Source Separation: Using Statistical charecterastic of the data to perfrom this source separation.   
        Not the inferential statistics i.e p-value or F-value but descriptive statistics i.e variance,covariance,spectral features.  
        Statisctical source separation that leads to temporal or spectral and spatial source separation.  
        Statistical source separation is all about applying filters to the data.  
        
        
  ## Source separation via Filtering
   #### Temporal Filtering :OrigionalSignal*Kernel=Filtered Signal - over time for one channel
   ####  Spatial Filtering : W^T*X; over space for all channel at one time point
-Temporal filtering is almost same as spectral filtering.
-Perfect source separration is not possible -mixed in spectrum
Source separation is based on the assumption that those sources has differemnt signature in the spectrum 


*`Notes are based on https://youtu.be/ukjuFUghieg `

------------------------------------------------------

# Origin,Sigificance and Interpretation of EEG

*Origin advantages, and limitation of EEG

Only if thousands of cells contribute thier small voltage is the signal large enough to reach the scalp surface.


## Advajntages of EEG
-Direct meausre of electrical brain activity
-Temporal resolution and pricision match the speed of cognition : 1data point every millisecond
-Richness of the data allow for physiologically inspired analyses(oscillation,synchronization,connectivity,complexity/scale-free)
-Link finding across scales/methods/species : electrical activity are conssistent across different shape of brain

## Disadvantages of EEG
-Limited to large-scale potentials
-Uncertainiites in anatomical localization
-Data(mdim,noises),analysis,and analysis, and visualization are complicated,time-consuming,and annoying
-High temporal precision and resolution - while studying slower cognitive process-read prara and conclude we don't know when that happend

* Notes based on https://youtu.be/Bmt89hHyxuM
------------------------------------

# Overview of Possibole Preprocessing Steps
- A list of possible steps of preprocessing electrophysiology data
- Multiple reminders that data preprocessing is often data-,study-,and lab-specific.


## Prepocessing vs Processing(Analyzing)
Preprocessing  is everything that you have to do to the data in order to get to the point where you can start to actually process or analyze the data.
Proprocessiing : Time consuming,tedious, Not Science, probably not fun. Do it well- do it once

Processing: Hypothesis driven, Exploratory, The meat of science, Hopefully lots of fun, Often done multiple times.

### Possible preprocessing steps
    import data into MATLAB
    high-pass filter(e.g, 5hz)
    import channel locations
    referencew EOG,ECG<EMG
    Epoch data around important events
    Subtract pre-stimulus baseline
    Adjust marker values
    Manual trial rejection
    Mark bbad electrodes
    Average reference EEG channels
    RUN ICA to clean data
 
