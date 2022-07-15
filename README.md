# Maven Airline Customer Satisfaction Analysis; A Survey Data
Cleaning,analysing and visualisation were done using PowerBI
# Introduction
This project is inspired from a challenge by MavenAnalytics on twitter.
The documentation includes;
   * Goal Of The Analysis
   * Data Transformation & Modelling
   * Power Pivot
   * Results
   * Conclusion
# Goal Of The Analysis
The aim of the analysis is to draw insights from the raw data provided, by evaluating the customers satisfaction level with the services administered by the organisation.
# Data Transformation & Modelling
Data was collected from MavenAnalytics,it contains responses from customers.The data was cleaned in power query,modelled into Fact and Dimensions tables. The tables created were;
 * Fact table: It contains all responses provided by the clients
 * Dim Flight Delay: It contains responses on Depature delay and Arrival delay.
 * Dim In-flight services: It contains responses on questions related to services offered on the airplane.
 * Dim Airport services: It contains responses on questions related to services administered in the airport.
 ![DATA MODEL](https://github.com/DeborahAkinyeye/DeborahAkinyeye-2.github.io/blob/main/Data%20modelling%20for%20maven.JPG)
 
 # Power Pivot
The overall customer satisfaction score (CSAT) was calculated using (Number of satisfied customers/Number of survey responses)*100

CSAT Was also calculated for Dim In-flight services and Dim Airport services;
* In-flight rating=( Number of satisfied customers/ Dim in-flight services[count]) 
Where Number of satisfied customers= Calculate(Count(Dim In-flight [ID], Dim In-flight services[response]>3)
* Airport rating= ( Number of satisfied customers/ Dim Airport services[count])
Where Number of satisfied customers= Calculate(count(Dim Airport [ID], Dim Airport services[response]>3).
# Results
![DASHBOARD](https://github.com/DeborahAkinyeye/DeborahAkinyeye-2.github.io/blob/main/updated%20analysis.JPG)

* From the analysis, a total of 129,880 people filled the survey
* Overall, 43% were satisfied and 57% were dissatisfied
* Customers were majorly satisfied with the seat comfort for In-flight services
* For the Airport services, Customers were majorly satisfied with baggage handling
* Departure and arrival time convenience had a poor rating of 5.14%, Online boarding 2.37% and Ease of booking 4.37%
* The Wi-fi service had a poor rating of 3.02% and the leg room service had an unsatisfactory rating of 9.93%.
# Conclusion
The purpose of CSAT surveys is to measure customers happiness with an organisation performance. The only factor that makes one airline significantly different from the other is the quality of customer service( in-flight service and Airport service)
The organisation should address the factors that influences the dissatisfaction from the customers. The "Recommendations" are included on the DASHBOARD.


