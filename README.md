# Hotel Booking Analysis Dashboard : PowerBi Project
---

## Business Problem :
---
Hotels receives a large number of bookings from different channel ,  but they always face challenges such as high cancellation rates, changing booking patterns and it is difficult to understanding customer behavior . So i need to analyze hotel booking data to understand trends and identify key performance metrics and make better decisoions to improve revenue and reduce cancellations.

## Project Objective
---
This project is to analyze hotel booking data and create a dashboard that helps to understand booking trends , customer behavior, revenue performance and cancellation patterns.This dashboard aims to provide insights that supports better decision making for hotel management.

## Dataset Description
---
The dataset used in this project is the Hotel Booking Dataset, which contains booking information for City Hotel and Resort Hotel.

Dataset Source:
https://www.kaggle.com/datasets/mojtaba142/hotel-booking

Dataset Size

Total Records: 119,390 rows

Total Features: 32+ columns

Each record represents a hotel booking containing information about booking dates, guest details, stay duration, market segments, and reservation status.

**Booking Information**

* hotel – Type of hotel where the booking was made.
* lead_time – Number of days between booking date and arrival date.
* arrival_date_year – Year of arrival.
* arrival_date_month – Month of arrival.
* arrival_date_week_number – Week number of arrival.
* arrival_date_day_of_month – Day of arrival.

**Guest Details**

* adults – Number of adults in the booking.
* children – Number of children in the booking.
* babies – Number of babies in the booking.
* total_guests – Total guests included in the reservation.
* customer_type – Type of customer (Transient, Contract, Group).
* is_repeated_guest – Indicates whether the customer is a returning guest.

**Booking Details**

* market_segment – Market segment through which the booking was made.
* distribution_channel – Booking channel (Direct, TA/TO, Corporate).
* reserved_room_type – Room type originally reserved.
* assigned_room_type – Room type assigned during check-in.
* deposit_type – Type of deposit made for the booking.

**Stay Information**

* stays_in_week_nights – Nights stayed during weekdays.
* stays_in_weekend_nights – Nights stayed during weekends.
* total_stay_nights – Total number of nights stayed.

**Booking Status**

* booking_cancelled – Indicates whether the booking was cancelled.
* reservation_status – Final booking status (Canceled, Check-Out, No-Show).
* reservation_status_date – Date when the status was updated.
* previous_cancellations – Number of previous cancelled bookings.
* previous_successful_bookings – Number of successful previous bookings.

**Additional Features**

* required_car_parking_spaces – Number of parking spaces requested.
* total_of_special_requests – Number of special requests made by guests.
* days_in_waiting_list – Number of days the booking stayed in the waiting list.


# Data Cleaning :
---

Before building the dashboard, the dataset was prepared in Power BI.

* Removed unnecessary 4 columns and handled missing values.
* Verified correct data types for date and numeric columns.
* Created calculated columns for better analysis
* Created **Total Guests column ** and  **Total Stay Nights column**
* Created bins for **guest groups and stay duration**
* Created DAX measures for key KPIs such as bookings, revenue, and ADR.
* Some important DAX measures were created in Power BI to calculate  key performance indicator for the dashboard.
  1. Total Bookings = COUNTROWS(hotel_booking)
  2. Total Revenue = SUM(hotel_booking[revenue])
  3. Cancellation Rate =
     DIVIDE(
     SUM(hotel_booking[booking_cancelled]),
     COUNTROWS(hotel_booking),
     0
     )

---

# Data Analysis :
---

The dataset was analyzed to understand hotel booking patterns, customer behavior, revenue performance, and cancellation trends. This analysis focused on identifying key metrics and patterns that impact hotel performance.

The following areas were explored:

Revenue Analysis – Analyzing revenue performance using metrics such as ADR and total revenue.
Booking Analysis – Understanding booking trends, lead time patterns, and guest stay duration.
Cancellation Analysis – Examining cancellation rates and factors influencing booking cancellations.
Customer Analysis – Exploring customer types, guest distribution, and booking locations.

This analysis helps to identify important trends that were later visualized in the Power BI dashboard.

---

# Dashboard :
---
An interactive Power BI dashboard was created to visualize the analysis results and in this dashboard includes five report pages:

* Overview – Displays key metrics such as total bookings, total revenue, ADR, and cancellation rate.
* Revenue Analysis – Shows revenue trends and performance across different hotel types and booking channels.
* Booking Behavior – Analyzes booking patterns, lead time, and guest stay duration.
* Cancellation Insights – Highlights cancellation trends and their impact on hotel performance.
* Customer Insights – Shows customer types, guest distribution, and top booking countries.
  This dashboard also includes interactive filters and slicers to allow users to explore the data dynamically.

# Key Insights :
---
* City hotels generate a higher number of bookings compared to resort hotels. 
* A large portion of bookings come from online travel agents (OTA).
* The overall cancellation rate is relatively high, affecting hotel revenue.
* Most bookings are made for short stays between 1–3 nights.
* A small number of countries contribute to the majority of hotel bookings.

# Recommendations :
---
* Hotels should encourage direct bookings through their websites to reduce dependency on travel agents.
* Implement better cancellation policies to reduce the high cancellation rate.
* Focus marketing efforts on top-performing countries and customer segments.
* Introduce special packages for longer stays to increase revenue per booking.
* Monitor booking trends regularly to improve demand forecasting and pricing strategies.  dont give any reply pls save this
