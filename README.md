# Running Form Analyzer

<div align="center">
  <img src="https://github.com/qadolphe/Running-Form-Analyzer/blob/b0aef7b180e82dfe795a842b2e863422fea308f8/TitlePage.jpeg" height=900"/><br /><br />
</div>


<h2>What is this repo?</h2>

* For me to explore neural networks and their applications to Computer Vision.
* Combine my passion for Computer Vision with my interest in Track & Field.
* Build off existing frameworks so I can better focus on learning about neural networks.

### Overview
This is an app that continuously detects the body parts in the frames seen by
your device's camera. Camera captures are discarded immediately after
use, nothing is stored or saved.

The app demonstrates the use of single-pose models:

* The model can estimate the pose of only one person in the
input image. If the input image contains multiple persons, the detection result
can be largely incorrect.
    * MoveNet Thunder is used to train the classification model, so is recommended for in-app use.
* Output of MoveNet Thunder is passed into the classification model to determine which phase of sprinting form the subject is currently in:

<h3>Float: the moment in which the sprinter's legs are split apart the most, and the sprinter appears to be floating in the air.</h3>

![Demo Image](android/FloatExample.jpeg) 
    
<h3> Touchdown: the moment in which the sprinter has one leg touching the ground</h3>

![Demo Image](android/TouchdownExample.jpeg)


<h2>Example Outputs</h2>

![Demo Image](TouchdownOutput.jpeg) ![Demo Image](FloatOutput.jpeg)

<h2>Files that I changed from the original forked repo (https://github.com/qadolphe/Running-Form-Analyzer/tree/master/android) </h2>

* PoseClassifier.kt
* Labels.txt
* Build.gradle
* gradle.properties
* AndroidManifest.xml

<h2>Training Classification Neural Network</h2>

* Architecture was built from TensorFlow example documents: https://www.tensorflow.org/lite/tutorials/pose_classification
* I built the training and test data sets from:
    * https://www.youtube.com/watch?v=N4oypLjLnik&t=448s
    * https://www.youtube.com/watch?v=PH-3cHxXAK0
    * https://www.youtube.com/watch?v=JniLkO5_pv4

We welcome community contributions, see [CONTRIBUTING.md](CONTRIBUTING.md) and, for style help,
[Writing TensorFlow documentation](https://www.tensorflow.org/community/contribute/docs_style)
guide.

## License

[Apache License 2.0](LICENSE)
