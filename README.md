# Taiwanese-Soap-Opera-Speech-Emotion-Recognition
This is the brief introduction. For the thorough process, results, and findings of this project, please refer to Report.pdf.

Distinguish emotions from Taiwanese soap opera lines with several different approaches
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

 
 
