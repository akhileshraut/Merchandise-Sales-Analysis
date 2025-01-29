# Merchandise-Sales-Analysis

### **Overview** 

This **Merchandise Sales Analysis** explores sales performance across different products, customer types, and locations. It helps identify which products are selling well, who the main customers are, and how location impacts sales. By analyzing trends, customer feedback, and shipping details, this report highlights key insights to improve pricing, inventory management, and customer experience. The goal is to provide clear, data-driven recommendations to boost sales and business efficiency.

### **Objective**

The objective of this **Merchandise Sales Analysis** is to evaluate sales performance across different product categories, customer segments, and regions. This analysis aims to:

- Identify top-performing products and sales trends.
- Understand customer purchasing behavior based on demographics.
- Assess the impact of international shipping on total sales.
- Analyze customer feedback and sentiment to improve product offerings.
- Provide data-driven recommendations to optimize pricing, inventory, and marketing strategies.

### **Key Goals**

The key goals of this analysis are:

- **Sales Performance Evaluation**: Identify trends and patterns in sales by product category, location, and customer demographics.
- **Customer Insights**: Understand the behavior of customers based on gender, age, and location to guide marketing efforts.
- **Sentiment Analysis**: Analyze customer feedback and sentiment scores to gain insights into product satisfaction and areas of improvement.
- **International Sales Impact**: Assess the effect of international shipping on sales performance and profitability.
- **Product & Price Optimization**: Identify high-performing products and assess the impact of pricing strategies.
- **Actionable Recommendations**: Provide strategic recommendations to enhance sales, improve inventory management, and refine marketing strategies.



### **Quantifiable Findings**

1. **Sales Performance**
   - **Total Sales**: $X,XXX,XXX (Total sales across all products and categories)
   - **Top Product Category**: *Clothing* (Contributed X% of total sales)
   - **Top Performing Product**: *Product A* with $XXX,XXX in sales (X% of total sales)
   - **Sales Growth**: X% increase in sales from Q4 2023 to Q1 2024

2. **Customer Demographics**
   - **Top Buyer Gender**: *Female* (X% of total orders from female buyers)
   - **Top Buyer Age Group**: *25-34 years* (X% of total sales)
   - **Top Order Location**: *New York City* (Contributed X% of total sales)

3. **Sentiment Analysis**
   - **Overall Positive Sentiment**: X% of customer reviews had a positive sentiment score.
   - **Negative Sentiment Products**: *Product B* had a negative sentiment score of X% with a direct correlation to a sales decline of Y%.

4. **International Sales**
   - **International Orders**: X% of total orders were shipped internationally, contributing $XXX,XXX in total sales.
   - **Impact on Revenue**: International orders had an average order value of $X,XXX, compared to domestic sales with an average of $X,XXX.

5. **Pricing Analysis**
   - **High-Price Range Sales**: Products priced above $X generated X% of total sales.
   - **Discount Effectiveness**: Discounted products accounted for X% of total sales, with an average discount of X%.

6. **Sales Efficiency**
   - **Sales per Unit**: X units sold per product on average, with the highest-selling product achieving X units sold.
   - **Shipping Charges Impact**: Orders with international shipping charges had an average additional revenue of $X,XXX.



### **Sentiment Analysis**

As part of the analysis of customer reviews, I began by conducting **Sentiment Analysis** to classify the sentiment of customer feedback. I utilized the **VADER (Valence Aware Dictionary and sEntiment Reasoner)** sentiment analysis tool due to its effectiveness in dealing with social media-style text and short sentences, such as customer reviews.

#### **Approach**

1. **Sentiment Classification**  
   VADER categorizes sentiments into three primary classifications:
   - **Positive**: Indicating a favorable opinion or sentiment.
   - **Neutral**: Indicating a neutral or mixed sentiment.
   - **Negative**: Indicating a negative or dissatisfied sentiment.

2. **Sentiment Scores**  
   VADER also provides a **sentiment score** that quantifies the intensity of sentiment. The score ranges from -1 (most negative) to +1 (most positive), where:
   - A score above 0.05 indicates a **positive sentiment**.
   - A score below -0.05 indicates a **negative sentiment**.
   - A score between -0.05 and 0.05 is considered **neutral**.

3. **Application of VADER**  
   The customer reviews in the **Merchandise Sales** dataset were processed using VADER to classify the reviews into positive, neutral, and negative categories based on the sentiment scores.

#### **Results**

- **Sentiment Distribution**  
  After applying VADER, I analyzed the sentiment distribution for each product category and customer segment. This helped to identify customer satisfaction levels, highlighting areas for potential improvement in product offerings and customer service.

- **Sentiment Score Range**  
  The **average sentiment score** was calculated for each review and aggregated at the product level to understand which products were positively or negatively received by customers.

#### **DAX Calculation for Sentiment Score**

Using the sentiment classifications from VADER, I created a **DAX measure** to calculate a weighted sentiment score, which considers the impact of each product's sales in relation to its sentiment.

```DAX
Sentiment Score = 
CALCULATE(
    AVERAGE('Merchandise_sales'[Sentiment Score]),
    'Merchandise_sales'[Sentiment] = "Positive"
)
```
#### **Dashboard Link**

https://app.powerbi.com/view?r=eyJrIjoiZGFhZDhkNGYtYzJjMi00ZTY4LWE5NjYtNzMxMDEzMWU1Nzk3IiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9

![Executive Summary](https://github.com/user-attachments/assets/89f172c5-06b1-4218-9d3e-a2bbaf4f8504)

![Product Performance](https://github.com/user-attachments/assets/429f7273-9b11-4d9a-bc1f-8207dfad9f02)

![Regional Analysis](https://github.com/user-attachments/assets/36b9d256-11c4-4044-8e57-22ceb82b0216)

![Customer Feedback](https://github.com/user-attachments/assets/0983a2b9-e2f7-449c-84c9-abfd2200c395)

