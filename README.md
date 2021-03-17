This project use the Keras lib for face recognition. The dataset use the Wild face recognition dataset.
1)	Set up the environment through installing packages:
	keras - deep learning
	scikit-learn - general purpose machine learning
	imbalanced-learn - methods that address class imbalance problem
2)	Verify that GPU available: for that notebook is available "CPU" with memory limit: 268435456 and "GPU" with memory limit: 14674281152
3)	Import packages that be used:
	numpy - linear algebra
	keras - deep learning
	sklearn.dataset - to download Labeled Faces in the Wild dataset
	sklearn.model_selection - for dataset train/test split
	sklearn.metrics - to measure the performance of our classifier
	matplotlib.pyplot - showing images and plots
	imblearn.over_sampling - random oversampling method to handle class imalance
4)	Download 4 files from http://scikit-learn.org/stable/modules/generated/sklearn.datasets.fetch_lfw_people.html:
	number of examples: 3023
	dimensionality of images: (154, 154, 3)
	number of unique classes (people): 62
5)	Plot a histogram showing how many examples per class (person) has.
6)	Display a random image together with its label (Igor Ivanov)
7)	Deep learning:
i)	import layer objects from Keras
ii)	define model: It consists of 10 convolutional layers with increasing number of filters (from 12 to 48). Every second layer has kernels of size `(2, 2)` with strides `(2, 2)` and serves the purpose of a trainable pooling layer since it reduces spacial dimensionality. Add Dropout for regularization which sets 50% of randomly chosen activations to 0. Add the last convolutional layer for dimensionality expansion to match the number of classes that we predict. Apply global average polling to squash spacial dimenaions.
iii)	create a DataGenerator object that will add some data augmentation to prevent overfitting
8)	Training with 100 epochs and save the trained weights to Google Drive.
9)	Results and analysis of the model:
i)	Plot training history size 720x720
ii)	Run predictions from the test set to visualize the results (overall accuracy is 85%)
iii)	Plot chart True label (Predicted Label). The labels are the names of the people whose pics on images. The darker square on the chart shows more correct predictions for true value.
iv)	Plot chart which showing accuracy of image recognition. Average accuracy is 81 %. Images which have higher accuracy also had darker squares on previous chart. 
