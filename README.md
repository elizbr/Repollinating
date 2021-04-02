# Repollinating
Making Room for Random: An Argument Against Best Fit in Music Recommendation 

There are a few separate files for code in this project. 
Here is a guide for what each does and if any data is specifically required. 

DATA 

A
sampler_671.csv —> the sample of data used throughout the project 
                                   
B
 indreams_merged.csv , losingawholeyear_merged.csv, oundandround_merged.csv —> 
These files represent the cleaned and formatted Spotify API track info results I have. 
There is one file per seed track and the method membership is annotated with the column ‘tracker’ 


CODE

#1 
EDA_003.ipynb
 	DATA REQUIRED:  ‘df1.csv’ (not included in zip due to size; inquire for access)
	CONTENT: takes 1/3 of the original million song dataset and creates a subset to be used for the rest of the project. The selection of the subset is based on a nodelist. Instead of including samples randomly, the output data-subset contains all tracks that fit into a slightly more defined network. 
	OUTPUT: “sampler_671.csv” (used in following files) 

#2 
methods.ipynb 
 	DATA REQUIRED:  ‘sampler_671.csv (included)
	CONTENT: creates tracks based on approach methods. 
	Including network approach, clustering, LSI, manual approach and more. 
	OUTPUT: lists of tracks based on each recommendation method 

   ^^^
In between this step and the next, I **manually** created Spotify playlists with the contents of each method’s recommendations and pulled their track info from the Spotify API. If you want to see my work converting json results to usable DFs in pandas, please inquire. (For the sake of being concise, I am omitting that work from my deliverable.) 
   ^^^

#3 
evaluation.ipynb 
 	DATA REQUIRED:   indreams_merged.csv , losingawholeyear_merged.csv &
	roundandround_merged.csv (included)
	CONTENT: scores and creates visuals to show findings of quantitative scoring of 
	variance between methods’ recommendations.  
	OUTPUT: graphs for average variance per scoring metric as well as graphs for 
	variance between the three seed song results per scoring metric 

PRIMARY LIBRARIES NEEDED
	MATPLOTLIB
	SEABORN 
	PANDAS
	NUMOY
	SKLEARN 
	NETWORKX
	NLTK 
	GENSIM
