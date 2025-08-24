# Uber Data Analysis

## 1. Background  
This project focuses on analysing Uber ride data to understand booking behaviour, cancellation reasons, payment preferences, vehicle usage, and rating patterns.  
The objective is to generate meaningful insights from exploratory data analysis (EDA) using Python and visualisation libraries.



## 2. Dataset Overview  
The dataset contains ride-related details such as:  
- Booking ID, Status, and Value  
- Pickup and Drop locations  
- Vehicle Type  
- Ratings (Driver and Customer)  
- Payment Method  
- Reasons for cancellation (Customer/Driver)  
- Ride Distance and Time  

A combination of preprocessing, grouping, and feature engineering was applied to prepare the data for analysis.



## 3. Data Preprocessing  
- Converted `Time` column into hourly features.  
- Subsetted relevant columns for cancellation and rating analysis.  
- Grouped values for frequency counts (e.g., by `Vehicle Type`, `Payment Method`).  
- Handled missing values where necessary.  



## 4. Visualisations & Insights  

### 4.1 Incomplete Rides Reasons  
- **Insight:** The major reason for incomplete rides is **customer demand**.  

![Incomplete Rides Reasons](images/incomplete_rides.png)  



### 4.2 Customer Cancellation Reasons  
- **Insight:** Most common reasons: **wrong address** and **change of plans**.  

![Customer Cancellation Reasons](images/customer_cancel.png)  



### 4.3 Driver Cancellation Reasons  
- **Insight:** Key factors: **customer-related issues** and **customer was sick**.  

![Driver Cancellation Reasons](images/driver_cancel.png)  


### 4.4 Driver Ratings (Boxplot)  
- **Insight:**  
  - Interquartile range (IQR) shows average rating ≈ **4.25**.  
  - Outliers: **3.0–3.75** and **4.5–5.0**.  

![Driver Ratings Boxplot](images/driver_ratings_box.png)  



### 4.5 Driver Ratings by Vehicle Type  
- **Insight:**  
  - Most drivers rated **4.3**.  
  - **Auto** has the highest ratings, followed by **Go Mini** and **Go Sedan**.  

![Driver Ratings by Vehicle](images/driver_ratings_vehicle.png)  



### 4.6 Customer Ratings by Vehicle Type  
- **Insight:**  
  - Majority of customers rated **4.9 and 4.6**, especially for **Auto, Go Mini, Go Sedan, and Bike**.  
  - Outlier ratings: **3.0–3.5**.  
  - Indicates overall customer satisfaction with drivers and ride experience.  

![Customer Ratings by Vehicle](images/customer_ratings_vehicle.png)  



### 4.7 Payment Methods  
- **Insight:**  
  - **UPI** is the most used payment method.  
  - Followed by **Cash** and **Uber Wallet**.  

![Payment Methods](images/payment_methods.png)  



### 4.8 Vehicle Type Usage  
- **Insight:**  
  - Most used vehicles: **Auto** and **Go Mini**, followed by **Go Sedan**.  

![Vehicle Usage](images/vehicle_usage.png)  



### 4.9 Vehicle Type vs Payment Method  
- **Insight:**  
  - Across all vehicle types, **UPI** is the most preferred, followed by **Cash** and **Uber Wallet**.  
  - **Auto, Go Mini, and Bike** dominate UPI usage.  
  - **Cash** is more common in Auto, Go Mini, and Go Sedan.  

![Vehicle Type vs Payment Method](images/vehicle_payment.png)  



### 4.10 Booking Value vs Minimum Ride Distance  
- **Insight:**  
  - A **minimum ₹50** booking corresponds to a **2.27 km ride distance**.  

![Booking Value vs Min Distance](images/booking_min_distance.png)  



### 4.11 Booking Value vs Maximum Ride Distance  
- **Insight:**  
  - Maximum ride distance can still be availed at **₹50** in certain cases.  

![Booking Value vs Max Distance](images/booking_max_distance.png)  



### 4.12 Pickup–Drop Mode & Frequency  
- **Insight:**  
  - Pickup–drop analysis highlights strong ride demand corridors.  
  - Frequent drop locations are concentrated around popular pickup hubs.  

![Pickup Drop Frequency](images/pickup_drop.png)  



### 4.13 Hourly Booking Distribution  
- **Insight:**  
  - Peak booking hours: **3:00 PM – 8:00 PM**.  
  - At **10 AM**, Auto bookings are nearly equal to Go Mini.  
  - Drop observed around **12 PM**, followed by a sharp rise after **3 PM**.  

![Hourly Booking Distribution](images/hourly_bookings.png)  



## 5. Conclusion  
The analysis highlights the following key findings:  
- **Customer demand** is the primary factor for incomplete rides.  
- **Wrong address** and **change of plans** drive cancellations by customers.  
- **Customer-related issues** are the main driver cancellation reasons.  
- **UPI dominates** payment preferences, especially for Auto and Go Mini rides.  
- **Auto and Go Mini** are the most popular vehicle choices.  
- **Peak demand** occurs in the evening (3–8 PM).  
- Both **drivers and customers maintain strong rating averages**, reflecting overall satisfaction.  

