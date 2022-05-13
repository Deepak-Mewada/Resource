# Neural Time series Analysis - MX Cohen

## Neuroscience is Source Separation
All mental process are happening together. Signal multiple sourcesso the goal is to separate the multiple sources.
Source separation as diagram:- True Sources (Latent constructs) -> Sensosrs (manifest variables) -> "Sources" components\
![image](https://user-images.githubusercontent.com/61898308/168231272-c3032f33-cd7f-4f54-8f2f-c172dc5d687d.png)

## How can source be separated?
-Anatomical Source Separation : based on anatomy,just study one part of the brain based on anatomy e.g study amagdala  
-Cognititve Source Separation : cleaver experiment to isolate a single cognitive source like short term mempory  
-Temporal Source Separation :  
-Spatial Source Separation :  
-Statical Source Separation: Using Statistical charecterastic of the data to perfrom this source separation.   
        Not the inferential statistics i.e p-value or F-value but descriptive statistics i.e variance,covariance,spectral features.  
        Statisctical source separation that leads to temporal or spectral and spatial source separation.  
        Statistical source separation is all about applying filters to the data.  
        This course is all about "temporal filter9ing"
        
  ## Source separation via Filtering
  ![image](https://user-images.githubusercontent.com/61898308/168231517-ce0ed4b0-d5a9-42ae-81d9-6acee3a7b7e0.png)

   #### Temporal Filtering : fig- OrigionalSignal * Kernel = Filtered Signal ; over time for one channel
   ####  Spatial Filtering : W^T * X ->analysis -> results; over space for all channel at one time point,
   SF instead of taking the time series from one single electrode and weighting time points over time 
      we are computing the spatial filter at each time point so we have each individual channel multipolied by a weight and then we sum up over all thge channel.
-Temporal filtering is almost same as spectral filtering.

### Assumption for Spectral separation
![image](https://user-images.githubusercontent.com/61898308/168231022-d5aedc7c-81c0-4964-b43a-261f7e6595fe.png)

graph - Power vs frequency
-slow frequency low fluctuations in signal ,fast frequency -high fluctuation in signal
-Perfect source separration is not possible -mixed in spectrum(10-18 hz)
Source separation is based on the assumption that those sources has differemnt signature in the spectrum 


*`Notes are based on https://youtu.be/ukjuFUghieg `

------------------------------------------------------

# Origin,Sigificance and Interpretation of EEG

*Origin advantages, and limitation of EEG
-Also valie for EMG,LFP

## What do EEG data look like 
![image](https://user-images.githubusercontent.com/61898308/168232819-90937763-9047-4714-a2e4-92c2cd206a6e.png)
-Volatage activity from population of nbeurons
-some poattern of activity are comnsistent across electrodes
-very often with EEG if you see unique activity on 1 electrode that you don;t see on any other electrode it's probably some noise contamination
-Person looking at screen various things are happenings:picture appear,button press

## Origin of the existence of EEG
![image](https://user-images.githubusercontent.com/61898308/168233873-9c5a1023-5ae7-453e-90a5-f7d1cb39f093.png)
Only if thousands of cells contribute thier small voltage is the signal large enough to reach the scalp surface.
![image](https://user-images.githubusercontent.com/61898308/168234128-39d03393-1e7b-48ad-805c-b31307314ebe.png)

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
 
