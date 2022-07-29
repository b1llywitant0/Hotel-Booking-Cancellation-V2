# Hotel-Booking-Cancellation

This notebook serves as an improvement of the training project of hotel booking cancellation prediction. This model use more data and features in the dataset, with refined background and more explanation at each notebook's section.

<p align="center">
<img src="https://github.com/b1llywitant0/Hotel-Booking-Cancellation/blob/main/Data/Hotel%20Header.jpg">
</p>


## Background
<p align='justify' style="font-weight: bold;">
Let's say that we have a hotel business to run. Since it is a business that revolve around service, customer satisfaction is the most important factor that indicates our success and future prospect of the business. Good experience will lead to good reviews, it will help us in developing loyal customer and searching for new customers. Increase in customers drives most businesses, it will lead to increase in revenue and business growth, that we can increase the quality of service and also expand our business. It is basically a snowball effect.

First impressions are crucial in business because it's a human nature to make judgment about someone in their first meet. Making a strong first impression will help the business develop customer relationships and sales. In hotel business, preparing for the arrival of the customers is important to develop a strong first impression. However, how does the hotel management distinguish between customers that will come or not based on their characteristics in booking application?

In this project, I will aid the hotel management to predict which customers that will cancel their booking based on their booking application characteristics. With this predictive machine learning model, it will lead to cost-efficiency of the hotel management in preparing the customers arrival and increase in customers satisfaction based on the strong first impression provided.
</p>

## Dataset Source
<p align='justify' style="font-weight: bold;">
This is a real-world data of customers, obtained from 2 hotels which are located in Portugal: Resort Hotel at the resort region of Algarve and City Hotel at the city of Lisbon. You can download it from <a href="https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand">Kaggle</a>. The dataset initially consists of 119,390 rows with 32 columns.
</p>

## Data Cleaning and EDA
<p align='justify' style="font-weight: bold;">
Detailed data cleaning and EDA can be read at <a href="https://github.com/b1llywitant0/Hotel-Booking-Cancellation-V2/blob/main/Hotel-Booking-Cancellation-Prediction-V2.ipynb">Jupyter</a>. The process of data cleaning eliminates 0.4% of data into 118,902 rows and only use 19 columns (1 label+18 potential features). 
</p>

## Insights
### How many bookings were canceled?
<p align="center">
<img src="https://github.com/b1llywitant0/Hotel-Booking-Cancellation-V2/blob/main/Pictures/Data%20imbalance.png" width="500" height="350">
</p>
<p align='justify' style="font-weight: bold;">
From the graph above, we can see the imbalance of the dataset. Considering the amount of 0 class is higher than class 1, we can use undersampling method such as Random Undersampler or Near Miss to balance the dataset for more unbiased result.
</p>

### Does waiting duration affecting the booking cancellation?
<p align="center">
<img src="https://github.com/b1llywitant0/Hotel-Booking-Cancellation-V2/blob/main/Pictures/Days%20in%20waiting%20list.png" width="500" height="200">
</p>
<p align='justify' style="font-weight: bold;">
Using hypothesis testing procedure (Mann-Whitney U), there was a signifant difference in median of days_in_waiting_list between 0 and 1 class, where class 0 (check-in) has longer duration of waiting. Thus, longer waiting duration didn't affect the booking cancellation. However, from this information, it is a precaution toward hotel owner to be able to give the best impression to those who waits longer. If failed, then it can easily turn into bad reviews for the hotel.
</p>

### 

## Prediction Results
### Benchmark Model
<p align="center">
<img src="https://github.com/b1llywitant0/Hotel-Booking-Cancellation/blob/main/Data/Hotel%20CV%20Results.png">
</p>
<p align='justify' style="font-weight: bold;">
Considering the mean score and its standard deviation, XGBClassifier was used.
</p>

### Hyperparameter Tuning
<p align='justify' style="font-weight: bold;">
Detailed hyperparameter tuning can be read at <a href="https://github.com/b1llywitant0/Hotel-Booking-Cancellation/blob/main/Supervised%20Model%20-%20Hotel%20Booking.ipynb">Jupyter</a>. 
</p>

### Test Data
<p align="center">
<img src="https://github.com/b1llywitant0/Hotel-Booking-Cancellation/blob/main/Data/Hotel%20Results.png">
</p>
<p align='justify' style="font-weight: bold;">
After hyperparameter tuning, this prediction model can identify which booking will be cancelled with good F1-score (0.8695).
</p>

# Conclusion
We can use this model to predict hotel booking cancellation of resort hotels in Portugal.
