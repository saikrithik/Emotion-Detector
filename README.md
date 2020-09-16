# Emotion-Detector
Emotion-Detector to detect angry,sad,disgust emotions.
## Dependencies
* Python 3, [OpenCV](https://opencv.org/), [Tensorflow](https://www.tensorflow.org/)
* To install the required packages, run `pip install -r requirements.txt`.
## Data Preparation (optional)
* The [original FER2013 dataset in Kaggle](https://www.kaggle.com/deadskull7/fer2013) is available as a single csv file. I had converted into a dataset of images in the PNG format for training/testing and provided this as the dataset in the previous section. 
* In case you are looking to experiment with new datasets, you may have to deal with data in the csv format. I have provided the code I wrote for data preprocessing in the `dataset_prepare.py` file which can be used for reference.
* Download the FER-2013 dataset from [here](https://drive.google.com/file/d/1X60B-uR3NtqPd4oosdotpbDgy8KOfUdr/view?usp=sharing) and unzip it inside the `src` folder. This will create the folder `data`.
* If you want to train this model, use:
* **[Reference](https://github.com/atulapra/Emotion-detection)**
## Algorithm
* First, the **haar cascade** method is used to detect faces in each frame of the webcam feed.
* The region of image containing the face is resized to **48x48** and is passed as input to the CNN.
* The network outputs a list of **softmax scores** for the seven classes of emotions.
* The emotion with maximum score is displayed on the screen.
