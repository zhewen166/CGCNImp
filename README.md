# CGCNIml
## KDD CUP 2018 Dataset
The KDD dataset is a public meteorologic dataset that comes from the KDD CUP Challenge 2018 $\footnote{KDD CUP. Available on: http://www.kdd.org/kdd2018/, 2018.}$. The KDD dataset collects air quality and weather data which was hourly collected between 2017/1/20 to 2018/1/30 of Beijing. Each record contains 12 attributes,for example PM_{2.5}, PM_{10}, CO, weather, temperature etc. The KDD dataset is an environmental monitoring dataset. In our experiment, the KDD dataset is used to simulate the data of bird habitat monitoring, and the imputation of the KDD dataset is more difficult as compared with bird habitats, the environment of kdd data is more complicated. We select 11 common features for our experiments as the previous method did. The dataset is about 15\% missing values. We split this dataset for every hour, and then for every 48 hours, we impute these time series with different models and calculate the imputation performance by the root mean squared error (RMSE) and Mean Absolute Error (MAE) between original values and imputed values.

## Bird Migration Dataset in China
The Birds Migration Dataset comes from the project Strategic Priority Research Program of Chinese Academy of Sciences, Grant No. XDA19020400. 
The Bird Migration Dataset collects migration trace data which was hourly collected between 2017/12/30 to 2018/5/10 of Anser fabalis and Anser albifrons. Each record contains 13 attributes,for example longitude, latitude, speed height,speed velocity, heading, temperature etc. We select 10 common features for our experiments. The dataset is about 10\% missing values. We split this dataset for 5 minutes, and then for every 5 minutes, we impute these time series with different models and calculate the imputation performance by the root mean squared error (RMSE) and Mean Absolute Error (MAE) between original values and imputed values. 
## Implementations Details
All the experimental results in this article are obtained under the same experimental environment. Detailly, the hardware is Intel i7 9700k, 48GB memory, NVIDIA GTX 1080 8GB, and the deep learning framework is PyTorch1.7 and TensorFlow1.15.0.

To maintain the same number of training and test samples as the contemporary method, the dataset was split with 80% of the records used for the training set and the remaining 20% used for the test set. 
All values are normalized in the range of 0 to 1. For training dataset, 10\% of the data in the training set was deleted. When testing dataset, we deleted between 10% and 90% of the  data, tested each method at a range of levels of missing data.
