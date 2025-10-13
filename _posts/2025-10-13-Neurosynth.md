# Neurosynth

## Objective
The objective of Neurosynth was to create a real-time emotion to synth sound classifier.

## Tech Stack
- Tensorflow
- OpenCV
- pyaudio

## Technique
Neurosynth was at its heart a convolutional neural net in Tensorflow, that used a vast input of labelled emotion pictures to classify a frame captured using the computer vision library OpenCV. This classification was then fed into pyaudio, where based on the emotion 
a synth sound played. The mapping of emotions followed typical convention, i.e. minor chords for sad or angry faces, and major chords for happy faces.

## Challenges
With this being my first CNN project, learning how to take in the facial input was difficult. Training required several forms of augmentation to reduce overfitting in the model. Procuring quality emotion images was also difficult, with several datasets being used.

## Lessons Learned
This project provided valuable lessons in ensuring data quality, and tuning neural networks. Its very important with especially a CNN to strike the bias-variance balance. A deep model likely over-trains on the patterns in the training data, and a shallow model likely doesn't learn deep enough patterns to make accurate predictions.

## Further
Going further in the project, we'd like to improve the real-time aspect of the predictions. As of right now, the image is only captured once every 1-2 seconds, which limits how fluid the synth outputs are. We'd also like to improve the variability of these outputs, making the chords flow into each other so it sounds musical.
