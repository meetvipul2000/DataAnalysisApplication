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
   - 

    coupon accepted ratio = total accepted population /  total coupon issued * 100
   
3) Visualize Coupon column
   -
   Following chart display coupon distrubution among different redeem locations.

   ![coupon_distribution_count](https://github.com/meetvipul2000/MachinLearningApplication/assets/7953100/cc9b7e26-28cd-494c-acd2-2f310b100c92)

   According to above chart most coffee house and max 20  Restaurant coupon issued higher compare to others.
       
4) Visualize the temparature column
   -
   Plotted histogram for different temprature coupon issued and coupon issued at higher temprature which mostly tells us summer period.
   Also we added coupon acceptance/rejection dimention in histogram and found that summer period coupn redumption is higher.
      
   ![Data_Distribution_by_Temperature](https://github.com/meetvipul2000/MachinLearningApplication/assets/7953100/0419b13f-bd60-47d4-b62f-c0c2c1d708bb)

6) Bar Coupon Invstigation
    -
    Bar coupon acceptance Ratio
   
          Bar Coupn Acceptance Ratio = ( Accepted Bar Coupon count / Total bar coupon issued ) * 100

          Bar coupon acception ratio : 41.19% 
          
    *** Compare the acceptance rate among all bar visitors ***

            Steps to find the result :
                  1. Filter the data with just bar coupon with accepted coupon data.
                  2. group the accepted coupon count by "Bar" column and count the total accepted coupon
                  3. find the total accepted bar coupon count.
                  4. divide the each group created in step 3 with total accepted coupon count to find the acceptance ratio for each "Bar"  group.
        
   ![pie_bar_coupon_acceptance_rate_by_bar_visitor_freq](https://github.com/meetvipul2000/MachinLearningApplication/assets/7953100/be74d5e3-bfec-450f-bfa1-5e50fcb3f95f)
        
        
                 Pie chart says that visitor visting less than month or 1-3 times a month accepting coupon more. Frequent 
                 drinker does not care about the coupon.
   
     *** Compare the acceptance rate between those who went to a bar 3 or fewer times a month to those who went more ***

            Steps to find the result :
                  1. Filter the data with just bar coupon with accepted coupon data.
                  2. rename the column name of "bar" column in a such a way so it creates only two distinct values.
                     first visitor visting 3 or fewer time and other is visiting higher than 3 times month.
                  3. Follow the same steps above to find the accedptance ratio of these 2 groups and plt the pei chart.

   ![pie_bar_coupon_acceptance_rate_by_bar_visitor_less_or above_3_times_month_freq](https://github.com/meetvipul2000/MachinLearningApplication/assets/7953100/a22fc6d4-fd60-4988-9f93-38e5c6252663)

            Pie chart indicates that 81.3% percetage of acceptance ratio of vistor visting bar less than 3 months
            which we already notice in previous study also.

     *** Compare the acceptance rate between drivers who go to a bar more than once a month and are over the age of 25 to the all others ***

          Steps to find the result :
                  1. Filter the data with just bar coupon with accepted coupon data.
                  2. Query the data with driver goes once a month and age over 25 nd count the total count.
                  3. count the other population subtracting filtered  (step 2 query) count from total count (step 1 query)
                  4. find the percentage of given criteria and other population.

   ![pie_bar_coupon_acceptance_rate_btn_more_than_once_bar_visitor_age_25_more_with_others](https://github.com/meetvipul2000/MachinLearningApplication/assets/7953100/5dd83b48-fe55-4175-bdc2-eb0ff9fe9e15)


     *** compare the acceptance rate between drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry ***
          Steps to find the result :
                  Follow the same steps as above to see the comparision.

   
8) 

9) 
   

10) 
    
11) 
12)   

13) 
14) 



**Sharing  results**
