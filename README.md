# COVID-19-FACO-CNN
The Idea of FACO is to develop digital healthcare solutions(app) to assist doctors and empower patients to diagnose and manage disease such as corona and stop it from spreading by using just a smartphone.
A diagnosis of respiratory disease is one of the most common outcomes of visiting a doctor. Respiratory diseases can be caused by inflammation, bacterial infection or viral infection of the respiratory tract. Diseases caused by inflammation include chronic conditions such as asthma, cystic fibrosis, COVID-19 and chronic obstructive pulmonary disease (COPD). Acute conditions, caused by either bacterial or viral infection, can affect either the upper or lower respiratory tract. Upper respiratory tract infections include common colds while lower respiratory tract infections include diseases such as pneumonia. Other infections include influenza, acute bronchitis, and bronchiolitis. Typically, doctors use stethoscopes to listen to the lungs as the first indication of a respiratory problem. The information available from these sounds is compromised as the sound has to first pass through the chest musculature which muffles high-pitched components of respiratory sounds. In contrast, the lungs are directly connected to the atmosphere during respiratory events such as coughs.
These audible sounds, used by our app, contain significantly more information than the sounds picked up by a stethoscope. Our approach is automated and removes the need for human interpretation of respiratory sounds. Plus, we can see lots of spreadable diseases nowadays such as HIV, Coronavirus, etc., so we have to track those patients to stop them from spreading
Implementation of a convolutional neural network used to identify wheezes and crackles in an audio file which is fed Mel-Spectrograms as inputs. During processing, audio clips are copied to 5 second long buffers, and are split into multiple segments if necessary, with zero padding added to fill the rest of the buffer. During training, Mel-Spectrograms are transposed and wrapped around the time-axis to help allow the network to learn to identify features occurring at arbitrary times within the recording. Data augmentation was employed in the form of audio stretching (speeding up and down) as well as Vocal Tract Length Perturbation, especially for the scarcer 'wheeze' and 'wheeze and crackles' classes. A one hot data labelling scheme was chosen as earlier attempts at using a multi-label scheme using a Sigmoid output layer resulted in poor training results (which in hindsight may have been caused by an excessively high learning rate). Currently, both the 'wheeze' and 'wheeze and crackles' classes pose the greatest challenge in the area of classification, and frequently produce false negatives, as indicated by the poor recall scores. Overall validation accuracy currently stands at roughly 70%.
