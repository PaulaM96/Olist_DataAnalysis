# Olist_DataAnalysis
> :construction: Project under construction :construction:
### This is a project of EDA and RFM segmentation using Kmeans
<p align="middle">
<img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/rfm-analysis-1024x550.png" width="480"> </p>
The objective of this project is to identify and segment potential customers to address personalized strategies to boost sales and increase revenue.

<h2> Purchases Historic</h2>
<p align="middle">
<img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/revenue.png" width="580" a> 
</p>
The highlight occurs in November 2017, whose sales increase may be related to a marketing action or black friday, for example. It is noted that from this period onwards, there was a significant increase in the number of requests.

<h2> Revenues Historic </h2>
<p align="middle">
<img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/faturamentoporano.png" width="580"> 
</p>
Taking into account that the last record in the base is dated August 29- 2018, as shown in the revenue per year chart, the revenue obtaining 8% up on the previous year.

<h2> Purchase Behavior </h2>
<p align="middle">
<h3>-Top 10 Categories with the most requests</h3>
</p>
<img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/10catcommaispedidos.png" width="800"> 
The chart above determines the category with the highest number of orders. However, the main objective of this analysis is to determine which product per category achieves the number of sales acceptable to the target, but due to lack of information, it is not possible to identify it.

<h3>-Distribution of orders by day of the week</h3>
<p align="middle">
<img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/diadasemana.png" width="580"> 
</p>
The flow of purchases tends to increase during weekdays

<h3>-Distribution of orders by time of the day</h3>
<p align="middle">
<img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/pedidosporhora.png" width="580"> 
</p>
<h3>-Distribution of payment types by month</h3>
<p align="middle">
<img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/download.png" width="860"> 
</p>
</p>
<h3>-Number of customers X Revenue</h3>
<p align="middle">
<img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/qtd_clientes_mes.png" width="480"> <img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/receita_mes.png" width="480"> 
</p>
The graphs above demonstrate that the total amount collected in the analyzed period has a degree of dependence proportional to the number of purchases made by new customers in e-commerce. However, according to Kotler's sales theory, competitive disadvantage occurs when the company's profit depends on the entry of new customers rather than their loyalty.

Satisfied customers become brand advocates, or in other words, true “sellers” and pass them on to contacts, family and friends. This generates savings in resources that would otherwise be spent on marketing and can be invested in other priorities.

Retaining customers in the company provides benefits in the medium and long term. Therefore, the problem that we aim to solve with this analysis is to segment customers so that we can define personalized strategies to retain each group of customers.

<h2> Segmentation using RFM</h2>

<p align="middle">
<img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/segmentos1.png" width="580"> 
</p>

The term RFM comes from the junction of three acronyms: Recency, Frequency, and Monetarity, seeking to better understand the customer and verify when was his last purchase, how many times he has bought and how much he has spent with the company. 

Recency(R) Days since the customer's last purchase Frequency(F) Number of products bought by the customer Monetarity(M) Total spent on purchases

RFM model is based on customer buying behavior, but for that, it is necessary to define a score.

<h3>Customer Score and groups</h3>

The customer score ranges from 1 to 5, where the higher this number, the better. This score is assigned for each acronym independently:

The more recent the customer's purchase the higher the Recency (R) score.
The more purchases the customer makes, the higher the Frequency score (F)
The more the customer spends on purchases, the higher the score the customer will have Monetarity(M)

 <table>
  <tr>
     <td>Group</td>
     <td>Description</td>
     <td>Range of R values</td>
     <td>Range of F and M Average</td> 
  </tr>
  <tr>
     <td>Champions</td>
     <td>Recently bought, return often and spend a lot</td>
     <td>4 - 5</td>
     <td>4 - 5</td> 
  </tr>
  <tr>
     <td>Loyal Customers</td>
     <td>They are customers who spend well and frequently</td>
     <td>2 - 5</td>
     <td>3 - 5</td> 
  </tr>
  <tr>
     <td>Potential Loyalist</td>
     <td>Recent buyers with a good average of amount spent and frequency</td>
     <td>3 - 5</td>
     <td>1 - 3</td> 
  </tr>
  <tr>
     <td>Customers Needing Attention		</td>
     <td>They are customers who bought recently, but they may have doubts whether they will make the next purchase in the company or a competitor</td>
     <td>2 - 3</td>
     <td>2 - 3</td> 
  </tr>
  <tr>
     <td>About to Sleep		</td>
     <td>These are customers who, although not buy a long time ago, can still buy again.</td>
     <td>2 - 3</td>
     <td>0 - 2</td> 
  </tr>
  <tr>
     <td>At Risk		</td>
     <td>Spend little, buy with frequently and haven't returned for a long time</td>
     <td>0 - 2</td>
     <td>2 - 5</td> 
  </tr>
  <tr>
     <td>Hibernating		</td>
     <td>Bought a long time ago few times and spent little</td>
     <td>1 - 2</td>
     <td>1 - 2</td> 
  </tr>
 </table>
 Now, let's take a look in our features distribution to create the segmentation.
<table>
  <tr>
    <td>Recency</td>
     <td>Frequency</td>
     <td>Monetary</td>
  </tr>
  <tr>
    <td>Time since last purchase</td>
     <td>Number of orders placed by each customer</td>
     <td>Total spent by this customer</td>
  </tr>
  <tr>
    <p align="middle">
      <td> <img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/recencia.png" width="300" /> </td>
      <td> <img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/frequencia.png" width="300" /> </td>
      <td> <img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/monetary.png" width="300" /> </td>
    </p>
  </tr>
 </table>

To define customers scores from 1 to 5, we used the K-means algorithm, grouping each variable (RFM) by their similar characteristics. <br>
The clusters of R are ordered by the lowest recency values ​​and are scored in descending order. <br>
The F and M clusters are ordered by the highest values ​​and are scored in descending order, respecting their respective variables (Frequency and Monetary).<br>

 <h3>Segmentation results</h3>

<p align="middle">
<img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/segmentos.png" width="620"> 
</p>

Based on our customers scores, this is the groups more relevants to the e-commerce in that period.

<h3>Proposed Suggestions</h3>
Selling more to the same consumers, receiving referrals and having revenue predictability are advantages of customer loyalty. 

Based on the distribution of groups, a transformation flow can also be set up by applying customized strategies for each group and increasing the conversion rate and customer interaction.
<p align="middle">
<img src="https://github.com/PaulaM96/Olist_DataAnalysis/blob/main/folder/fluxo.png" width="580"> 
</p>

Therefore, according to the segmentation presented, we suggest some strategies that can be addressed in each group.

**70.65% Loylist Potential:**
This group is made up of recent buyers, who have a good average spend and frequency.
It is a group with a lot of potential, as customers who have had a recent positive experience with the company may be interested in making new purchases.
Some strategies that might be interesting
* Personalized product recommendations for example; 
* Offer a loyalty program or discount vouchers; 
* Keep these potential customers engaged with the brand;

**14.77% About To Sleep:**
These are customers who, although they haven't bought in a long time, can still buy again.
This group needs attention, as it is the second segment with the most customers. It is necessary to regain the interest of these people in the company.
Some strategies that might be interesting
* Popular product recommendations and promotions; 
* Personalized communications targeted to the customer's profile;

**10.98% Hibernating:**
These are customers who bought a long time ago, only once or a few times and spent little.
This group needs to be worked on so that the company becomes interesting again so that it is loyal.
Some strategies that might be interesting
* Offers of relevant products and good deals; 
* Offer submission communications;

**1.61% Customer Needing Attention:**
These are customers who have recently purchased, but may still have doubts whether they will make their next purchase from the company or a competitor.
This group needs actions so that they can perceive that the company can offer the best conditions and meet all their expectations.
Some strategies that might be interesting
* Promotional campaigns for a limited time, which create the sensation of unmissable; 
* Show the advantages that your company offers; 
* Product recommendations based on your behavior;

**1.33% At Risk:**
These are customers who spend little money and buy frequently, but haven't bought in a long time.
This group shows a portion of customers that over time lost interest in the company. It is necessary to regain the attention of these companies
Some strategies that might be interesting
* Sending personalized communications and messages to get closer to the customer; 
* Offer good deals;

**0.64% Loyal Customers:**
These are customers who spend well and often
This group includes customers who already believe in the company. It is necessary to maintain this relationship so that it evolves to a greater recency, and they become Champions customers.
Some strategies that might be interesting
* Personalized communication; ○ Avoid sending generic bulk offers; 
* Offer few products, but present products they are likely to be interested in; 
* Implement some reward for reviewing products and reviews so that they are willing to express their positive experiences and motivate other buyers;

**0.03% Champions:**
These are customers who have purchased recently, buy frequently, and spend a lot. True indirect sellers of the brand, and the main objective should be to increase this group more and more.
They are brand advocates. It is necessary to maintain this relationship so that the customer remains engaged.
Some strategies that might be interesting
* Special offers, products and discounts for these customers to make them feel valued; 
* Avoid sending generic bulk offers; ○ Personalized communications; 
* Rewards; 
* Ask for opinions and feedback to show that his opinion as a customer matters;

<h3>References</h3>

As dicas de Philip Kotler para a fidelização de clientes. Retrieved from: https://www.nitronews.com.br/blog/dicas-de-philip-kotler-para-fidelizacao-de-clientes/ <br>
Exploring Customers Segmentation With RFM Analysis and K-Means Clustering. Retrieved from: https://medium.com/web-mining-is688-spring-2021/exploring-customers-segmentation-with-rfm-analysis-and-k-means-clustering-118f9ffcd9f0 <br>
O que é RFM e como aplica-lo ao seu time de Customer Success. Retrieved from: https://medium.com/maxmilhas-tech/o-que-%C3%A9-rfm-e-como-aplic%C3%A1-lo-ao-seu-time-de-customer-service-b9c35817ed01 <br>
RFM e como aplica-lo ao seu time de customer service. Retrieved from: https://medium.com/maxmilhas-tech/o-que-%C3%A9-rfm-e-como-aplic%C3%A1-lo-ao-seu-time-de-customer-service-b9c35817ed01 <br>
RFM Analysis for customer segmentation in ecommerce. Retrieved from: https://www.retailreco.com/blog/rfm-analysis-for-customer-segmentation-in-ecommerce/ <br>
RFM Analysis using python. Retrieved from: https://www.geeksforgeeks.org/rfm-analysis-analysis-using-python/ <br>
Stack Academy. Retrieved from: https://stack-academy.memberkit.com.br/ <br>



