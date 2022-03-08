# CGCNImp
All the experimental results in this article are obtained under the same experimental environment. Detailly, the hardware is Intel i7 9700k, 48GB memory, NVIDIA GTX 1080 8GB, and the deep learning framework is PyTorch1.7 and TensorFlow1.15.0.

To maintain the same number of training and test samples as the contemporary method, the dataset was split with 80% of the records used for the training set and the remaining 20% used for the test set. 
All values are normalized in the range of 0 to 1. For training dataset, 10\% of the data in the training set was deleted. When testing dataset, we deleted between 10% and 90% of the  data, tested each method at a range of levels of missing data.
