# Dialogue Act Recognition 


This repository aims to create a classification model for the task of Dialogue Act Recognition. In linguistics and in particular in natural language understanding, a dialog act is an utterance, in the context of a conversational dialog, that serves a function in the dialog. Types of dialog acts include a question, a statement, or a request for action. It helps in determining the function of a particular utterance in a dialogue and is thus extremely useful for spoken language understanding. 


## Dataset

The Switchboard Dialog Acts corpus was used for this task which consists of telephone speech which is annotated with dialog act tags. Along with this we also had the raw transcriptions corresponding to each sound file. 

## Feature Extraction 

To create the training data for the Dialog Acts recognition model, the first step was to extract the relevant features from the given dataset. The following sets of features were extracted:

* Textual features: For the textual features, the LIWC (Linguistic Inquiry and Word Count) features were extracted from the transcriptions. LIWC features groups words into psychologically motivated categories  such as ‘analytic’ , ‘authentic’, ‘clout’ etc

* Acoustic Features: These features were extracted from the sound files using a tool called ParselMouth. This consisted of traditional sound properties such as ‘Pitch’, ‘Intensity’ , ‘Harmonic Noise Ratio’, ‘Jitter’ etc. 


## Classification Model 

The given task was modelled as a 10-way classification problem by choosing the data points corresponding to the 10 most frequent act tags from the Switchboard corpus. 

Three different training datasets were constructed for training purposes:

* Textual Features
* Acoustic Features
* Textual + Acoustic Features 

For each of the above data set two different types of  models were trained and their accuracy was evaluated on a test set:

* Deep Learning Model
* XGBoost Model 


## Results and Conclusion

After conducting experiments with the two models on the three different training data sets, the best performance (classification accuracy) was obtained for the XGBoost model on the Textual + Acoustic Features training data set. An accuracy of 75\% was obtained using this model and feature set. 



