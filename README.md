# Taiwanese-Soap-Opera-Speech-Emotion-Recognition
This is the brief introduction. For the thorough process, results, and findings of this project, please refer to Report.pdf.

Distinguish emotions from Taiwanese soap opera lines with Convolution Neural Network models through several different approaches.
1. Categorical (labeled with five emotions)
2. Binary (labeled with two emotions)
3. Transfer Learning with [MiteshPuthran's model](https://github.com/MiteshPuthran/Speech-Emotion-Analyzer) as the base model

## Dataset
The dataset is entirely built (clipped) by us. Yet we do not own the original audio/video, and we only used this dataset for academic purposes. For more information, please refer to the license.
- They are mostly from the dramas 'Taiwan Tornado' (台灣龍捲風) and 'Family Reunion' (一家團圓) on YouTube. 
- 600 wav files in total, 001-500 for training and validation, 501-600 for testing
- Each file is exactly three seconds long
- Mostly in Taiwanese, some Mandarin

We labled the 600 files in two different ways, one with five emotions (label_categorical.csv) and the other with two emotions (label_binary.csv).
The binary label essentially turns the 'angry', 'sad', and 'fearful' in categorical label into 'negative' in binary label, and 'happy' and 'neutral' in categorical label into 'neutral' in binary label.
We actually tried listen to the clips again and relabel with binary, but after the first 100 clips we found out that the new label is the same as directly relabel from categorical.
 
 ## Results
 1. Categorical model only had 43.9% accuracy on testing data. 'angry' and 'neutral' has better accuracy, and according to the confusion matrix, if we only consider this two, it has 74% accuracy.
 ![image](https://user-images.githubusercontent.com/39045469/216509960-83f47c0d-4181-4928-98ba-21675efe3ce7.png)
 2. Binary model got 70.9% accuracy on testing data.
 3. Transferred model only got 25% accuracy on average for validation data.
 
 ## Discussion/Conclusion
 We concluded three main causes for the relatively low accuracy of our models, which are
 1. Existing datasets have fixed tones for certain emotions
 2. Complexity of emotions
 3. Visible difference in spectrogram
 
 For the complete details of these three, please refer to Report.pdf.
 
 ## Authors
 This project was done in collaboration with LIN Yi-Ting (林奕廷), HUNG Sheng-Hsiang (洪聖祥), ZHANG Hong-Qi (張紘齊), and HSU Chun (許淳).
