# Emotion Detector 

real-time facial emotion detection using deep learning. built this in my journalism class 
(yeah journalism) while my teacher was looking at all the code completely lost lmao. 
she was lowkey impressed tho so we move 💀

my laptop was COOKED. like genuinely about to combust. the fan was going insane the whole 
time it was training, i was just sitting there in class pretending everything was normal 
while my macbook was basically a space heater

## what it does

opens your webcam and detects your emotion in real time. slaps a bounding box on your face 
and tells you if you look angry, happy, sad, disgusted, scared, surprised or just completely 
neutral (me in every lecture)

7 emotions detected:
- 😠 Angry
- 🤢 Disgust
- 😨 Fear
- 😊 Happy
- 😐 Neutral
- 😢 Sad
- 😲 Surprise

## how it works

trained a CNN (convolutional neural network) on FER-2013, a dataset with like 35,000 
labelled face images. the model learns what each emotion looks like pixel by pixel. 
then opencv grabs your webcam feed, finds your face, and runs it through the model 
live in real time

## stack

- Python
- TensorFlow / Keras
- OpenCV
- NumPy

## how to run it yourself

- clone the repo: 
git clone https://github.com/annakashmiri/-emotion-detector.git
cd -emotion-detector
- install dependencies:
pip install tensorflow-macos tensorflow-metal opencv-python numpy matplotlib
- if you're not on a mac:
pip install tensorflow opencv-python numpy matplotlib
- download the FER-2013 dataset from kaggle and put it in a data/ folder, then train:
python train_model.py
- once training is done, run the live detector:
python detect.py

!!!!!!!! press Q to quit !!!!!!!!

## notes

- accuracy is around 60-65% which is actually normal for FER-2013, its a hard dataset
- good lighting helps a lot
- the model file (emotion_model.h5) is included so you can skip training and just run detect.py directly
- built this randomly one afternoon and it somehow worked

---

started as a vibe, ended with my laptop threatening to shut down. 10/10 would do again