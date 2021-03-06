# Telecom-Churn-Prediction
Mobicom Telecom Churn Rate Pridiction
All data files referenced in this assignment are in the Jigsaw lab at:

 

“C\Data Science with R\Assignments\Graded Assignment\Topic 13 – Capstone Project “

 (Please note that you will need to save all your work in C drive in your user folder)

 

At Mobicom, you are a business analyst and have been urgently called into a meeting with the marketing head and retention manager. The agenda of this meeting is to discuss the results of Industry survey reports that have been just released. In response to these reports, senior management at Mobicom is concerned that the market environment of rising churn rates and declining ARPU will hit them even harder as churn rate at Mobicom is relatively high. Currently they have been focussing on retaining their customers on a reactive basis when the subscriber calls in to close the account. But this alone does not seem to be enough and the management team is keen to take more initiatives on this front. One of these is to roll out targeted proactive retention programs, which include usage enhancing marketing programs to increase minutes of usage (MOU), rate plan migration, and a bundling strategy among others.  To be able to effectively drive these retention strategies, a few key questions of interest require urgent attention and you been given the task of showcasing data based insights and recommendations relating to subscriber churn.

Churn Market Survey Report

Mobile operators who lead in loyalty outperform their competition in network and service quality, as well as in customer care, according to the 2014 Acquisition and Retention Study Report from Nokia. While retention drivers vary by market maturity, delivering excellent quality keeps customers happy and loyal. The study results also show that churn continues to keep operators on their toes with 40% of customers globally planning to switch provider in the next 12 months. Cost and billing plays a key role across markets when deciding to stay with an operator, but is specifically important for emerging markets where 49% of customers consider it to be the most important factor when deciding to stay with an operator, with network and service quality following at 25%. When it comes to data usage, the number of subscribers experiencing problems is high.  Among the problems they report are slow download speeds (20%), data throttling (17%) and applications that don’t work (16%). Another key finding of the 2014 Acquisition and Retention Study Report is that recommendations from family and friends have gained in importance in the decision to switch operators. Subscribers who have switched operators in recent months reported two key information sources in their decision: the Internet and recommendation of family and friends.

Another report by Ovum forecasts a falling ARPU, which will continue to decline across all markets.

Proactive Retention Strategies

Usage based promotions to increase minutes of usage (MOU) for both voice and data. It is an accepted fact that low usage and high churn go hand in hand.

 

Rate Plan Migration is a strategy to move customers from non-optimal plans to optimal plans as it has been observed that subscribers on non-optimal rate plans have significantly higher odds of churn relative to subscribers on optimal rate plans.

 

Offer bundling and churn have been found to be negatively correlated. A family bundle is an option that is being considered especially in the light of one of the observations from the survey that referrals from family and friends are a deciding factor for switching carrier.

Definitions

Bundling A bundling strategy involves offering several products/services for sale as one combined

product (e.g., package deal), using demand for the dominant product to sell a secondary offer. This combined product is offered at a discount price so that it is cheaper to buy the bundle than products separately.

 

Optimal rate plan A post-paid wireless rate plan typically includes a fixed number of voice minutes that a customer can use per month. Usage exceeding the monthly allowance is called overage and is charged at a premium per-minute rate. Unless customers have a good understanding of their historical usage patterns and have the ability to predict their future wireless needs accurately, selecting an optimal rate plan to subscribe can be a challenging task. Conceptually, non-optimal rate plan subscribers could have saved money by switching to other more suitable plans to minimize overage. Specifically, customer’s rate plan suitability is determined based on their actual voice usage, the monthly rate of their selected plans, and the associated overage charges. Given that rate plan is not available on the data file, a proxy for non-optimal rate plan could be higher overage revenue as a percentage of total revenue.  

 

Artificial churn/spinners or serial churners “Artificial” churn may be encouraged by so called “spinners”, who disconnect and reconnect to the same network by taking advantage of offers available.

 

Top Line Questions of Interest to Senior Management:

What are the top five factors driving likelihood of churn at Mobicom?
Validation of survey findings. a) Whether “cost and billing” and “network and service quality” are important factors influencing churn behaviour.  b) Are data usage connectivity issues turning out to be costly? In other words, is it leading to churn?
Would you recommend rate plan migration as a proactive retention strategy?
What would be your recommendation on how to use this churn model for prioritisation of customers for a proactive retention campaigns in the future?
 

What would be the target segments for proactive retention campaigns? Falling ARPU forecast is also a concern and therefore, Mobicom would like to save their high revenue customers besides managing churn. Given a budget constraint of a contact list of 20% of the subscriber pool, which subscribers should prioritized if “revenue saves” is also a priority besides controlling churn. In other words, controlling churn is the primary objective and revenue saves is the secondary objective.
 

The data set named “telecomfinal.csv” is present here “C\Data Science with R\Assignments\Graded Assignment\Topic 13 – Capstone Project “

Data dictionary named “data_documentation.xls” is present here “C\Data Science with R\Assignments\Graded Assignment\Topic 13 – Capstone Project “

An approach note, “Final Case Study.pptx” is present here “C\Data Science with R\Assignments\Graded Assignment\Topic 13 – Capstone Project “

A sample data quality report named “Sample Data quality report.xlsx” is present here “C\Data Science with R\Assignments\Graded Assignment\Topic 13 – Capstone Project “

 

Your Answer:
What are the top five factors driving likelihood of churn at Mobicom?
Ans: From the summary of my final model, "Mod5".

The model results show that the top 5 factors affecting churn are:
 a. retdays_1 with beta coefficient of 0.65594746871
 b. unq_7 with beta coefficient of 0. 64967748241

c. unq_4 with beta coefficient of 0. 30160665676
 d.  ethnic_O with beta coefficient of 0.27496872141
 e. area_nrthwst with beta coefficient of 0.25741382589

The 1st Factor explains, with a unit increase in variable retdays, there is 0.65594746871 unit increase in churn.
The 2nd factor explains, with a unit increase in level 7 of variable uniqsubs, there is 0. 64967748241 unit increase
in churn.

Similar explaination applies to the next 3 variables.
var uniq_4 represents level 4 of variable uniqsubs,var ethnic_O represents var ethnic with level o,area_nrthwest represents Northwest/Rocky Mountain Area.
Var retdays_1 represents valid values for var retdays,i.e.values more than "0"

 

2. Validation of survey findings. a) Whether “cost and billing” and “network and service quality” are important factors influencing churn behaviour.  b) Are data usage connectivity issues turning out to be costly? In other words, is it leading to churn?

Ans:

The following variables explain "cost and billing" : 

Variables totmrc_Mean i.e. 'base plan charge' representing cost to customer, 
var rev_Range i.e. 'Range of Revenue(charge amount)' representing billing amount,var ovrrev_Mean = DATOVR_MEAN + VCEOVR_MEAN i.e. 'Mean overage revenue' (It is the sum of data and voice overage revenues) representing the overage revenue earned from customers after billing the same to them. 
and var totrev i.e. 'Total revenue' representing total revenue earned from customers.

var totmrc_Mean has beta coefficient value of -0.00611296994 meaning a unit increase in this variable is causing decrease in churn by 0.00611296994/unit.

var rev_Range has beta coefficient value of 0.00141700436 meaning a unit increase in this variable is causing increase in churn by 0.00141700436/unit

var ovrrev_Mean has beta coefficient value of 0.00843815335 meaning a unit increase in this variable is causing increase in churn by 0.00843815335/unit

var totrev has beta coefficient value of 0.00015313460 meaning a unit increase in this variable is causing increase in churn by 0.00015313460/unit

Having said that, if we notice above mentioned beta values, a unit increase in them is having almost 0% impact on churn. SO it seems cost and billing is not very important factors here influencing churn behaviour at Mobicom.

 

The following variables explain "network and service quality"

VARIABLE              BETA COEFFICIENT

mou_Range            0.000365011
change_mou          -0.000688095
drop_blk_Mean        0.007238319
drop_vce_Range       0.019625411 
mou_opkv_Range   -0.001002745 
iwylis_vce_Mean     -0.018229864
avgqty                     0.001218918 
avg6mou                -0.000277044
adjmou                   0.000022004
retdays_1                0.655947469
complete_Mean      -0.001636750

 

From the above statistics, data explains the following:

1. Variables mou_Range 1.e. with a unit increase in 'Range of number of minutes of use', there is increase in Churn by 0.000365011 units.
2. Var change_mou i.e. with a unit increase in 'Percentage change in monthly minutes of use vs previous three month average, there is decrease in Churn by -0.000688095 units.

Similar conclusions can be drawn for all the other variables as well.

Of the above variables, the beta coefficient of variable retdays_1 is expressing as a very important factor influencing Churn behavior. That is with the increase in the number of days since a customer makes a retention call, the customer's chances of churning is very high. This could probably be because their grievances are not being catered to properly. These customers should be paid more attention to and special offers should be made to them depending upon their grievances.

 

2b) Are data usage connectivity issues turning out to be costly? In other words, is it leading to churn?

comp_dat_Mean - Mean no. of completed data calls. 
plcd_dat_Mean - Mean number of attempted data calls placed
opk_dat_Mean - Mean number of off-peak data calls
blck_dat_Mean - Mean no. of blocked / failed data calls
datovr_Mean - Mean revenue of data overage. 
datovr_Range - Range of revenue of data overage
drop_dat_Mean - Mean no. of dropped / failed data calls

The above variables express data usage connectivity. 
quantile(tele$plcd_dat_Mean,prob=c(0.10,0.20,0.30,0.40,0.50,0.60,0.70,0.80,0.82,0.84,0.85,0.86,0.88,0.90,1))

The Data Quality Report for all the above variables show that only upto 15% customers are actually making data calls or using the internet.

So it would be good to work towards attaining more customers to use data and also towards proving quality network connectivity and service to provide maximum customer satisfaction and reduce Churn. Since there is not enough usable data for the other above variables they are not showing any influence 
on the Churn Behaviour at Mobicom.

 

 

3. Would you recommend rate plan migration as a proactive retention strategy?


Variable ovrrev_Mean has beta coefficient of 0.00843815335.
var ovrrev_Mean = DATOVR_MEAN + VCEOVR_MEAN i.e. 'Mean overage revenue' 
It is the sum of data and voice overage revenues representing the overage revenue earned from customers after billing the same to them. 
The Beta coefficient is not showing a strong impact of overage billing as an influencer of churn behaviour. 
Though this might be a matter of concern for few individual customers and they could be catered to on case to case basis. But overall rate plan migration as a proactive retention strategy might not help much at Mobicom.

 

4. What would be your recommendation on how to use this churn model for prioritisation of customers for a proactive retention campaigns in the future?

Gains Chart
library(gains)
gains(test$churn,predict(mod6,type="response",newdata=test),groups = 10)

the Gains Chart shows that the top 20% of the probabilities contain 29.1% customers that are highly likely to churn.


# Selecting Customers with high churn rate
test$prob<-predict(mod6,type="response",newdata=test)
quantile(test$prob,prob=c(0.10,0.20,0.30,0.40,0.50,0.60,0.70,0.80,0.90,1))

# Top 20% of the probabilities lie between 0.3060563 and 0.6878571

Applying cutoff value to predict customers who Will Churn
pred4<-predict(mod6, type="response", newdata=test)
pred4<-ifelse(pred4>=0.3060563 , 1, 0)
table(pred4,test$churn)

pred4    0      1

     0   11684 3234

     1   2401   1329


Targeted<-test[test$prob>0.3060563 & test$prob<=0.6878571 & test$churn=="1","Customer_ID"]
Targeted<-as.data.frame(Targeted)
nrow(Targeted) ==> 1329

write.csv(Targeted,"Target_Customers.csv",row.names = F)

Thus Using the model can be used to predict customers with high probability of Churn and extract the target list using their "Customer ID".

5. What would be the target segments for proactive retention campaigns? 

Solution:
pred5<-predict(mod5, type="response", newdata=test)
test$prob<-predict(mod5,type="response",newdata=test)
quantile(test$prob,prob=c(0.10,0.20,0.30,0.40,0.50,0.60,0.70,0.80,0.90,1))
pred6<-ifelse(pred5<0.20,"Low_Score",ifelse(pred5>=0.20 & pred5<0.30,"Medium_Score","High_Score"))
table(pred6,test$churn)

str(test$totrev)
quantile(test$totrev,prob=c(0.10,0.20,0.30,0.40,0.50,0.60,0.70,0.80,0.90,1))
Revenue_Levels<-ifelse(test$totrev<692.684,"Low_Revenue",ifelse(test$totrev>=692.684 & 
test$totrev<1051.643,"Medium_Revenue","High_Revenue"))

table(Revenue_Levels)

table(pred6,Revenue_Levels)

## Thus this table can be used to select the levels of customers are to be targeted and the Target list can be thus extracted:

test$prob_levels<-ifelse(pred5<0.20,"Low_Score",ifelse(pred5>=0.20 & pred5<0.30,"Medium_Score","High_Score"))
test$Revenue_Levels<-ifelse(test$totrev<692.684,"Low_Revenue",ifelse(test$totrev>=692.684 & 
test$totrev<1051.643,"Medium_Revenue","High_Revenue"))

Targeted1<-test[test$prob_levels=="High_Score" & test$Revenue_Levels=="High_Revenue","Customer_ID"]
Targeted1<-as.data.frame(Targeted1)
nrow(Targeted1) ==> 1561

write.csv(Targeted1,"High_Revenue_Target_Customers.csv",row.names = F)

 
