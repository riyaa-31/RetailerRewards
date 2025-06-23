## RetailerRewards
A Spring Boot REST API for calculating and retrieving rewards points based on customer id and transaction over the past three months

#A retailer offers a rewards program to its customers, awarding points based on each recorded purchase. A customer receives 2 points for every dollar spent over $100 in each transaction, plus 1 point for every dollar spent over $50 in each transaction (e.g. a $120 purchase = 2x$20 + 1x$50 = 90 points). Given a record of every transaction during a three month period, calculate the reward points earned for each customer per month and total.

- The package name is structured as com.retailer.rewards
- Used MySQL database to store the information
- Do run the script.sql on MySQL to prepare the test data
- In sql script, the DB consists of two tables , Customers and Transactions for maintaining record of customers and storing the Transaction details of each customer.
- Used Mockito , Junit library for unit testing


**Technologies Used**
- Java 8+
- Spring Boot 3.2
- MySQL
- Maven

**Tools Used**
- Intellij Ide Ultimate - for development of the project
- PostMan - for API testing

**API Endpoint**<br> 
Get Reward Points by Customer ID

**GET** `/customers/{customerId}/rewards`

**Response Example**
```json
{
  "customerId": 1001,
  "lastMonthRewardPoints": 120,
  "lastSecondMonthRewardPoints": 90,
  "lastThirdMonthRewardPoints": 150,
  "totalRewards": 360
}
```

 GET `http://localhost:8080/customers/{customerId}/rewards`
