# Neural Time series Analysis - MX Cohen

## Neuroscience is Source Separation
All mental process are happening together. Signal multiple sourcesso the goal is to separate the multiple sources.
Source separation as diagram:- True Sources (Latent constructs) -> Sensosrs (manifest variables) -> "Sources" components\
![image](https://user-images.githubusercontent.com/61898308/168231272-c3032f33-cd7f-4f54-8f2f-c172dc5d687d.png)

## How can source be separated?

- Anatomical Source Separation : based on anatomy,just study one part of the brain based on anatomy e.g study amagdala  
- Cognititve Source Separation : cleaver experiment to isolate a single cognitive source like short term mempory  
- Temporal Source Separation :  
- Spatial Source Separation :  
- Statical Source Separation: Using Statistical charecterastic of the data to perfrom this source separation.   
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
- Temporal filtering is almost same as spectral filtering.

### Assumption for Spectral separation
![image](https://user-images.githubusercontent.com/61898308/168231022-d5aedc7c-81c0-4964-b43a-261f7e6595fe.png)

graph - Power vs frequency
- slow frequency low fluctuations in signal ,fast frequency -high fluctuation in signal
- Perfect source separration is not possible -mixed in spectrum(10-18 hz)
Source separation is based on the assumption that those sources has differemnt signature in the spectrum 


*`Notes are based on https://youtu.be/ukjuFUghieg `

------------------------------------------------------

# Origin,Sigificance and Interpretation of EEG

*Origin advantages, and limitation of EEG
-Also valie for EMG,LFP

## What do EEG data look like 
![image](https://user-images.githubusercontent.com/61898308/168232819-90937763-9047-4714-a2e4-92c2cd206a6e.png)
- Volatage activity from population of nbeurons
- some poattern of activity are comnsistent across electrodes
- very often with EEG if you see unique activity on 1 electrode that you don;t see on any other electrode it's probably some noise contamination
- Person looking at screen various things are happenings:picture appear,button press

## Origin of the existence of EEG
![image](https://user-images.githubusercontent.com/61898308/168233873-9c5a1023-5ae7-453e-90a5-f7d1cb39f093.png)
Only if thousands of cells contribute thier small voltage is the signal large enough to reach the scalp surface.

## Origin of the content of EEG
![image](https://user-images.githubusercontent.com/61898308/168234128-39d03393-1e7b-48ad-805c-b31307314ebe.png)
Every lines ups and down in EEG signal shows instatntaneous activity of population of cells. 
- We have a good understanding of why EEG exists. That's not we are ointerested in neuroscientist,psychologist,
- What we are interested in is what these signals mean-wnot here exactly thye come from
- There is information that's computated in brain and that manifests as this volatge fluctuation in EEG signal
- Cognition,thinking,memories and perception and so on doesn't come from these large wiggles(signal) like these.
- Cognition is actually coming from the really complext dynamic interaction between different brain cell,regions,layers

*Existence of EEG is reletively well known but the content of EEG signal is really unknown. In order to understand the content we need to analyses EEG appropriately.

## Advajntages of EEG
![image](https://user-images.githubusercontent.com/61898308/168236213-48a26b3c-ba05-423f-aaa1-ae435d71ca08.png)
1.Direct meausre of electrical brain activity  
2.Temporal resolution and pricision match the speed of cognition(faster than 1 data point every millisecond) : 
        -Cognition happens at the speed of 10's of milli sec to 100's of mili sec to a few sec
        -So we have brain measurement method that can measure the brain at the same speed as cognition occures
3.Richness of the data allow for physiologically inspired analyses(oscillation,synchronization,connectivity,complexity/scale-free)   
-Extremly rich there are a lot of information that is packed in the EEG signals and this allows for many kind of analysis physiologoically inspired analyssis to be performed on the data    
4.Link finding across scales/different spatial & temporal scales/diff methods/diff species :   
![image](https://user-images.githubusercontent.com/61898308/168238893-61eaed76-f445-4ec7-9c9e-9075e12a1299.png)
Similar kind of patterns of electrical temporsal activity at many spatial scale of the universe of the brain -invidual neurons to cordinated activity of cells  
![image](https://user-images.githubusercontent.com/61898308/168238927-33e3de35-328d-4d6f-9635-fd74789dc675.png)  
- Electrical activity are conssistent across different shape of brain   
- We can measures gamma bends oscillation in human cats mice insects   
- honey bees have tiny brain brain exibit temporal patterns of electrical activity that seems to be really similar to ther pattern of electrical activity that we can measure in human.  
- We can access and study those consistent feature across evolution using electrophisiology.  

## Disadvantages of EEG
![image](https://user-images.githubusercontent.com/61898308/168240115-a705704e-bfd2-49bb-8406-0de89a9da468.png)

1.Limited to large-scale potentials : can't study the activity of singal neurons  
- Many computation happening at a spatial scale that is too small to read by EEG 
- Electrical fields from geomatrically opposing dipoles cancel out leading to zero change in voltage that you can measure with EEG
2.Uncertainiites in anatomical localization 
![image](https://user-images.githubusercontent.com/61898308/168241693-89af5dac-8abd-40af-89e3-cdd720da8d71.png)
- Not measuring electrical activity directly spatially directly from the brain it is electrical activity coming from the brain but we mesure it from the outside.
- Where does in the brain these EEg signal come from? Mathematical ways
![image](https://user-images.githubusercontent.com/61898308/168241756-89aea85c-0978-4679-9933-66bf39abe6eb.png)
- There are lot of uncertainities in these localization.
- there are already so much rich info in temporal,spectral,and spatial information in EEG that we no need to necesarilly need to estimate the physically location of  the brain signal  
 3.Data(mdim,noises),analysis,and analysis, and visualization are complicated,time-consuming,and annoying      
4.High temporal precision and resolution -can be good when when we know excatly when that process happened;  
- However while studying slower cognitive process we don't know excatly when that process happened -read para and come up with hypothesis-  
- excatly we dont know when they come up with hypothesis excatly at what time point - we don't know when that cognititve process happened     
 - Therefor temporal precision is a disadvantage
 
* Notes based on https://youtu.be/Bmt89hHyxuM
------------------------------------

# Overview of Possibole Preprocessing Steps  
- A list of possible steps of preprocessing electrophysiology data  
- Multiple reminders that data preprocessing is often data-,study-,and lab-specific.  


## Prepocessing vs Processing(Analyzing)
Preprocessing  is everything that you have to do to the data in order to get to the point where you can start to actually process or analyze the data.   
![image](https://user-images.githubusercontent.com/61898308/168257959-c622df84-3395-4156-a323-cada39cf4f77.png)

#### Proprocessiing : Time consuming,tedious, Not Science, probably not fun. Do it well- do it once   
#### Processing : Hypothesis-driven, Exploratory, The meat of science(real sceince), Hopefully lots of fun, Often done multiple times.  

## Possible preprocessing steps
![image](https://user-images.githubusercontent.com/61898308/168261390-1b5e7a25-a1ca-45c3-9601-b1ad7a46a368.png)

Ispiration-can be modidied according to study  

        -Import data into MATLAB   
        -High-pass filter(e.g, 0.5 Hz)   
        -Import channel locations   
        -Referencew EOG,ECG<EMG   
        -Epoch data around important events : 3D- Time, channel, epochs     
        -Subtract pre-stimulus baseline : eg.subtract avg voltage potential from each elexctord-all trial in same     
        -Adjust marker values : when specific event happenedcategorise, highlys tudy specific     
        -Manual trial rejection : reject trial with bad data-look at data is important
        -Mark bad electrodes :   noisy or broken electrodes 
        -Average reference EEG channels : head electrode,avoid single reference electrode,do after marking bad electrode  
        -RUN ICA to clean data    
        
 *`Notes based on  https://youtu.be/JMB9nZNGVyk?list=PLn0OLiymPak0t1moK3sn4Sl1seXlEOPHT
 
 ----------------------------------------------------------------------
 # Data Cleaning : Signal artifacts (not) to worry about

 ![image](https://user-images.githubusercontent.com/61898308/168262710-4b36299f-1695-4b20-a252-230b2c1a7740.png)
  -Artifact to worry anout and ignore  
  -visual based artifact rejection: look at data... big artifact and remove  
  -ICA can help to remove srtifact like blink - without having to remove the data   
  ![image](https://user-images.githubusercontent.com/61898308/168275635-6d71633e-3042-4423-b7ad-3b46123bc00c.png)
   ![image](https://user-images.githubusercontent.com/61898308/168282912-5dfb42e3-0339-47d1-b16a-bc2eeb4617f1.png)  
   Two kind or artifect: brief burst or long : may be muscle activity,scratch   
   -Wether to remove trial one - if study is all about frontal cortex processing you are not actually going to see data electrode from     back of head   
   -run independent componenent analysis and see if ICA removes that componenet   
   -F5 seems to be weird electrode - real brain activity+ noise: either completely remove or interpolate that component
                another solution is to run ICA and see if ICA can remove this artifact alone- work sometimes and doesn't work sometime     
                
 `Notes based on https://youtu.be/VDqwfP0mlfU?list=PLn0OLiymPak0t1moK3sn4Sl1seXlEOPHT`
 
 ---------------------------------------------------------------------------------------
 # Topographical Mapping and Spatial distributions  
 
 - Various ways of visualizing data over space.
 - How to interpret topographical maps. 
 ![image](https://user-images.githubusercontent.com/61898308/168286437-842611b1-505a-464b-a5dc-9c3edc243d8c.png)
- Two example of topographical map : looking down on womewons head
- Missing electrode
- Allow richness in data
- think to keep in mind : how can we draw a color if we don't have electrod at a place?
- This is done based on interpolation : assumption voltage value changes smoothly from one data point to another datapoint
- If we had measured data there how it would have been?
- These two maps from exactly same data just at two time points : Guess what was happening in both the experiments?
- 1st : Subject saw a visual stimuli is shown on computer screen then visula cortex litup
- 2nd : 

     
   
   

