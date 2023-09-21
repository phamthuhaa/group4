<html>
 <head>
  GROUP 4
 </head>
 <style>
body {
background-color:#fcdcf2;
}
</style>
 <body>
  <h1 style="font-size:40px;text-align:center;color:#704362;"> <b>MINI-PRESENT <br> BANK CUSTOMER CHURN </b></h1>
  <p style="font-size:24px;text-align:center;color:#704362;"> <i>Phạm Thị Thu Hà - Lê Thiên Nhi - Nguyễn Phan Hoàng Duy - Đinh Hoàng Dương - Trương Quang Duy - Hoàng Quang Minh </i></p>
  <h2> 1.INTRODUCTION </h2>
  <p>Churn prediction is the practice of determining which customers are most likely to discontinue or cancel their subscription to a service. This is an important consideration for many firms because obtaining new customers is more expensive than retaining existing ones..

Every year, the banking industry has one of the highest rates of client attrition. The expanding market competitiveness, which provides customers with more options and better offers, is one of the primary drivers of client attrition for retail banking firms. In order to detect early signs of potential customer churn, banks must obtain a full, 360-degree view of their client base and their interactions across several channels. They would be able to detect early warning signs of client churn, such as a decrease in transactions or a drop in sales..

This project uses customer data to analyze and anticipate customer attrition for 'ABC Multinational Bank,' a fictitious bank. The ABC Multinational Bank dataset shows which clients have left, stayed, or signed up for their services. Each customer has multiple critical demographics that can help us identify at-risk customers, pain spots, and actions to be performed...</p>
<img src="https://cdn.analyticsvidhya.com/wp-content/uploads/2019/05/customer-churn-edit.jpeg"/>
<h2> ABOUT DATASET </h2>
<p>This dataset is for ABC Multinational bank with following columns:
<br>
-customer_id, unused variable.
<br>
-credit_score, used as input.
<br>
-country, used as input.
<br>
-gender, used as input.
<br>
-age, used as input.
<br>
-tenure, used as input.
<br>
-balance, used as input.
<br>
-products_number, used as input.
<br>
-credit_card, used as input.
<br>
-active_member, used as input.
<br>
-estimated_salary, used as input.
<br>
-churn, used as the target. 1 if the client has left the bank during some period or 0 if he/she has not.
<br>
Aim is to Predict the Customer Churn for ABC Bank.</p>

<img src="./mini-present/1.png">
<img src="./mini-present/2.png">
<img src="./mini-present/3.png">
<img src="./mini-present/4.png">
<img src="./mini-present/5.png">
<h2> 2. DATA VISUALIZATION </h2>
<p>Data visualization is an important method in the data exploration process and conveying information. By using charts, graphs, and plots, we can visually display relationships, trends, and patterns in data. This helps us gain deeper insights into the data and make informed decisions based on that information.</p>
<img src="./mini-present/6.png">
<img src="./mini-present/8.png">
<img src="./mini-present/7.png">
<p>Most banks and financial institutions have adjusted and provided services such as personal loans, credit card facilities, and other loan packages, targeting individuals in the age range of 22 and above. From the initial data, we can observe a sharp increase, reaching its peak for the age group of 30-40, which consists of individuals with stable careers and finances. Subsequently, a significant decline in the data can be predicted as the age increases, as the purchasing and consumption habits and trends of this age group tend to decrease over time. They primarily prefer cash payments, resulting in lower credit scores.</p>
<img src="./mini-present/9.png">
<img src="./mini-present/10.png">
<img src="./mini-present/11.png">
<img src="./mini-present/12.png">
<img src="./mini-present/13.png">
<p>
 age = np.array([24,24,24,25,25,27,29,29,31,32,34,35,36,38,38,39,39,41,41,42,42,43,43,44,44,44,45,45,46,50,58])
balance = np.array([0.0,0.0,0.0,0.0,0.0,134603.88,59697.17,115046.74,102016.72,0.0,0.0,0.0,136815.64,0.0,0.0,0.0,0.0,0.0,83807.86,0.0,159660.8,125510.82,141349.43,0.0,113755.78,142051.07,0.0,143129.41,0.0,0.0,132602.88])

sorted_indices = np.argsort(age)
sorted_age = age[sorted_indices]
sorted_balance = balance[sorted_indices]

plt.figure(figsize=(12,7))

plt.plot(sorted_age, sorted_balance, linewidth=2.8)
plt.xlabel('Age')
plt.ylabel('Balance')
plt.show()</p>
<img src="./mini-present/14.png">
<p>
 First, we can see that ages with account balances ranging from 110,000 - 140,000 are distributed very evenly among different ages but mainly concentrated in the ages 25-30 and 41-45 years old. And the number of zero account balances also exists a lot in the range of 32 - 42 years old and from 46 - 50 years old.
</p>
<img src="./mini-present/15.png">
<p>
 age = np.array([24,25,27,29,31,32,34,35,36,38,39,41,42,43,44,45,46,50,58])
balance = np.array([0,0,134603.88,87371.955,102016.72,0,0,0,136815.64,0,0,41903.93,79830.4,133430.125,85268.95,71564.705,0,0,132602.88])

sorted_indices = np.argsort(age)
sorted_age = age[sorted_indices]
sorted_balance = balance[sorted_indices]

plt.figure(figsize=(10, 6))

plt.plot(sorted_age, sorted_balance)
plt.xlabel('Age')
plt.ylabel('Balance')
plt.show()
</p>
<img src="./mini-present/16.png">
<p>In the chart on the right, that's the average value of the account balance at each age. I will divide this chart into 2 age groups, first from 24-40 and then from 40-60</p>
<img src="./mini-present/16.png">
<img src="./mini-present/17.png">
<img src="./mini-present/18.png">
<img src="./mini-present/20.png">
<p>
 We can see that the number of people using both Credit Card and Active Mumber is 40%. This is followed by 40% of people using only 1 of the two categories. And the number of people who don't take both is 20%. Looking at the graph, we see that the number of people participating in the strategy is 80%, but there are still a few people who are not interested in this.
</p>
<h2> 3. CONCLUSION </h2>
<p>
 We can see that the number of people using both Credit Card and Active Mumber is 40%. This is followed by 40% of people using only 1 of the two categories. And the number of people who don't take both is 20%. Looking at the graph, we see that the number of people participating in the strategy is 80%, but there are still a few people who are not interested in this.
</p>
<h1 style=text-align:center;color:#704362,font-sixe:40px;"> <b>THANK YOU FOR LISTENING </b></h1>
 </body>
</html>
