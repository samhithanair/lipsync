# Lipsync Project 
#### By Samhitha Nair
In this project, I had used the concept of Wav2Lip to create a model that would overlay Hindi audio onto a video that originally had Telugu audio. The lips movements of the subject should also match the audio at the correct time. 

## Pre-requisites
 Before running the model, I cloned the Wav2Lip git and installed the requirements as per the text file given. I had also installed the necessary libraries and imported them.

## Language
Python - Google Colab

## Overview
Three classes were created - one to upload video, one to upload audio and one to render the result clip. 
Since the sample video had clips of where the face was not visible, I applied brute force methods by clipping the original video into those with and without face. I rendered the clips with the visible face along with their corresponding translated audio using GPU.
I then concatenated all the videos using moviepy 
Later in the future, I plan on incorporating a face recognition model to detect if a face is visible so that the lipsync can be carried out. If there is no visible face, the translated audio would continue to play until a face is recognized. 

### How to Use

* Upload the video required using the ```video.uploadVideo()``` block
* Upload the audio required using the ```audio.uploadAudio()``` block
* Render the final video by running the ```render.output()``` block
* Download each clip and input them into the last code block to get the final result

## License
Distributed under the MIT License. See ```LICENSE.txt``` for more information.

## Acknowledgements
The pre-trained model can be found [here](https://github.com/justinjohn0306/Wav2Lip)
