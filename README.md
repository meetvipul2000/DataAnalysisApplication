**Amazon Coupon Acceptance Data analysis**

**Context**

Imagine driving through town and a coupon is delivered to your cell phone for a restaraunt near where you are driving. Would you accept that coupon and take a short detour to the restaraunt? Would you accept the coupon but use it on a sunbsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaraunt? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?

Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?

**Objective**

The Objective this exercise to analysis the data and find  out the various attributes affecting the coupon acceptance and rejection. 

**Collecting the data.**

This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’. There are five different types of coupons -- less expensive restaurants (under $20), coffee houses, carry out & take away, bar, and more expensive restaurants ($20 - $50).


**Cleaning the data.**

Before I started analysing the data, started following data cleaning process.

First we ran the for loop for each of the columns to see how many null values exists for each column. this exercise led to perform cleaning of many and a single column which contains 90% of the data null.

After cleaning the dataset, data left with following shape.

(12079, 25) // (Row,Col)

**Data Analysis**

1) What Propostion of the  total population decided to accept coupon?

    coupon accepted ratio = total accepted population /  total coupon issued * 100
   
2) Visualize Coupon column
   
     - Following chart display coupon distrubution among different redeem locations.

       ![coupon_distribution_count](https://github.com/meetvipul2000/MachinLearningApplication/assets/7953100/cc9b7e26-28cd-494c-acd2-2f310b100c92)

   
4) 

5) 
    
6) 
7)   

8) 
9) 



**Sharing  results**
