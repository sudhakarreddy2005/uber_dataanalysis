# Uber Rides Data Analysis

## Overview
This project analyses Uber ride data to uncover insights into ride behaviour, cancellations, ratings, payment preferences, and vehicle usage. The dataset has been cleaned, concatenated, and structured for better analysis. Various statistical and visualisation techniques are applied to identify trends in customer and driver activity.



## Dataset Information
### Columns and Datatypes
- **Date**: object → Date of booking  
- **Time**: object → Time of booking (later converted to `datetime` for analysis)  
- **Booking ID**: object → Unique identifier for each booking  
- **Booking Status**: object → Status of ride (Completed / Incomplete / Cancelled)  
- **Customer ID**: object → Unique identifier for customer  
- **Vehicle Type**: object → Type of vehicle used (Auto, GoMini, GoSedan, Bike, etc.)  
- **Pickup Location**: object → Pickup location of the ride  
- **Drop Location**: object → Drop location of the ride  
- **Booking Value**: float → Value of the booking in INR  
- **Ride Distance**: float → Distance travelled in kilometres  
- **Payment Method**: object → UPI, Cash, Wallet etc.  
- **Driver Ratings**: float → Rating given to driver by customer  
- **Customer Rating**: float → Rating given by driver to customer  
- **Cancellation Reasons**: object → Reasons from both customer and driver perspectives  



## Insights and Analysis

### 1. Incomplete Rides Reasons
- **Observation:** The most common reason for incomplete rides is **Customer Demand**.  
- **Visualisation:**  
  ![Incomplete Rides](images/incomplete_rides_reason.png)



### 2. Customer Cancellation Reasons
- **Observation:** The top reasons for customer cancellations are **Wrong Address** and **Change of Plans**.  
- **Visualisation:**  
  ![Customer Cancellation](images/customer_cancellation_reasons.png)



### 3. Driver Cancellation Reasons
- **Observation:** The major driver-side cancellation reasons are **Customer Related Issues** and **Customer was Sick**.  
- **Visualisation:**  
  ![Driver Cancellation](images/driver_cancellation_reasons.png)



### 4. Driver Ratings Distribution
- **Observation:**  
  - The average rating (IQR) is **4.25**.  
  - Outliers exist at **3.0–3.75** and **4.5–5.0**.  
- **Visualisation:**  
  ![Driver Ratings Boxplot](images/driver_ratings_boxplot.png)



### 5. Driver Ratings by Vehicle Type
- **Observation:**  
  - Most drivers are rated around **4.3**.  
  - **Auto** drivers receive the highest number of ratings, followed by **GoMini** and **GoSedan**.  
- **Visualisation:**  
  ![Driver Ratings by Vehicle](images/driver_ratings_vehicle.png)



### 6. Customer Ratings by Vehicle Type
- **Observation:**  
  - Most customers provide ratings of **4.9** and **4.6**.  
  - Customers are generally satisfied with autos, GoMini, GoSedan, and bikes.  
  - Ratings in the **3.0–3.5 range** are considered outliers.  
- **Visualisation:**  
  ![Customer Ratings](images/customer_ratings.png)



### 7. Payment Methods
- **Observation:**  
  - **UPI** is the most popular payment method.  
  - Followed by **Cash** and **Uber Wallet**.  
- **Visualisation:**  
  ![Payment Methods](images/payment_methods.png)



### 8. Vehicle Usage
- **Observation:**  
  - The most frequently used vehicles are **Auto** and **GoMini**, followed by **GoSedan**.  
- **Visualisation:**  
  ![Vehicle Usage](images/vehicle_usage.png)



### 9. Vehicle Type vs Payment Method
- **Observation:**  
  - Across all vehicle types, **UPI** dominates, followed by **Cash** and **Wallet**.  
  - **Auto, GoMini, and Bike** are most often paid via UPI.  
  - With **Cash**, Auto, GoMini, and GoSedan dominate.  
- **Visualisation:**  
  ![Vehicle vs Payment](images/vehicle_vs_payment.png)



### 10. Minimum Ride Distance and Booking Value
- **Observation:**  
  - A minimum booking of **₹50** corresponds to a **minimum ride distance of 2.27 km**.  
- **Visualisation:**  
  ![Min Ride Distance](images/min_ridedistance.png)



### 11. Maximum Ride Distance
- **Observation:**  
  - Maximum ride distances are also available at **₹50**, showing variation in booking pricing.  
- **Visualisation:**  
  ![Max Ride Distance](images/max_ridedistance.png)



### 12. Pickup vs Drop Location (Most Frequent Drop per Pickup)
- **Observation:**  
  - Each pickup location has a **most frequent drop location**, helping understand popular ride flows.  
- **Visualisation:**  
  ![Pickup Drop Analysis](images/pickup_drop.png)



### 13. Hourly Booking Trends
- **Observation:**  
  - Peak booking times are between **3 PM to 8 PM (15:00–20:00 hrs)**.  
  - At **10 AM**, autos are nearly equal to GoMini rides.  
  - At **12 PM**, bookings decline but rise again post 3 PM.  
- **Visualisation:**  
  ![Hourly Bookings](images/hourly_bookings.png)





## Conclusion  
The analysis highlights the following key findings:  
- **Customer demand** is the primary factor for incomplete rides.  
- **Wrong address** and **change of plans** drive cancellations by customers.  
- **Customer-related issues** are the main driver cancellation reasons.  
- **UPI dominates** payment preferences, especially for Auto and Go Mini rides.  
- **Auto and Go Mini** are the most popular vehicle choices.  
- **Peak demand** occurs in the evening (3–8 PM).  
- Both **drivers and customers maintain strong rating averages**, reflecting overall satisfaction.  


## How to Use
1. Clone this repository.  
2. Open the Jupyter Notebook (`uber.ipynb`).  
3. Run all cells to reproduce the analysis and plots.  
4. Refer to the `images/` folder for saved visualisations.  



## Requirements
- Python 3.x  
- pandas  
- numpy  
- seaborn  
- matplotlib  
- jupyter  



## Author
Developed as part of a **Data Analysis Project** to explore **real-world ride behaviour in Uber datasets**.



