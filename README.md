# Online Ticket Booking Data Analysis: Customer Retention Study

## Project Overview

This project analyzes online movie ticket booking data to understand customer behavior, purchase patterns, campaign usage, and customer retention. The main objective is to explore how customers interact with the ticket booking platform and whether promotional campaigns are associated with repeat purchases.

The project focuses on cleaning raw transaction data, preparing an analytical dataset, performing exploratory data analysis, and building customer retention insights that can support business decision-making.

## Business Problem

Online ticket booking platforms often use promotional campaigns such as vouchers, direct discounts, and reward points to attract customers. However, promotions are only valuable if they help bring customers back and improve long-term retention.

This project aims to answer the following questions:

* Who are the customers using the platform?
* What are the common purchase behaviors by time, platform, and payment method?
* Which campaign types are used by customers?
* Do customers who use promotions come back for additional purchases?
* How does customer retention change over time?

## Dataset

The original dataset contains multiple related tables from an online movie ticket booking system:

* `customer.csv`: customer profile information
* `ticket_history.csv`: ticket transaction history
* `campaign.csv`: campaign and promotion information
* `device_detail.csv`: device and platform information
* `status_detail.csv`: transaction status descriptions

After cleaning and joining the tables, the main analytical dataset is saved as:

* `fact_ticket.csv`

This processed file combines ticket transactions with customer, campaign, status, and device information.

## Tools and Technologies

* Python
* Pandas
* Jupyter Notebook
* Matplotlib
* Seaborn
* Power BI
* GitHub

## Project Structure

```text
.
├── data/
│   ├── raw/
│   │   └── movie_ticket_data/
│   └── processed/
│       ├── campaign_clean.csv
│       ├── customer_clean.csv
│       ├── device_clean.csv
│       ├── fact_ticket.csv
│       ├── status_clean.csv
│       └── ticket_clean.csv
│
├── notebooks/
│   ├── 01_data_overview.ipynb
│   ├── 02_customer_profile.ipynb
│   ├── 03_purchase_timing.ipynb
│   ├── 04_customer_segments.ipynb
│   └── 05_customer_journey.ipynb
│
├── src/
│   └── make_processed_data.ipynb
│
└── Logic Chart.pdf
```

## Data Cleaning and Preparation

The raw data was cleaned and transformed before analysis. Key preparation steps included:

* Loaded multiple raw CSV files into Python
* Checked table structure, data types, missing values, and duplicate records
* Converted date and time columns into proper datetime format
* Removed invalid future dates from customer date of birth
* Removed duplicate ticket records
* Filled missing campaign values as `no_campaign`
* Filled missing device model and platform values as `unknown`
* Joined ticket, customer, campaign, status, and device tables into one analytical dataset
* Saved cleaned datasets into the `data/processed/` folder

The final processed dataset, `fact_ticket.csv`, is used for further analysis.

## Analysis Sections

### 1. Data Overview

The first notebook explores the raw dataset structure and prepares cleaned versions of each table.

Main tasks:

* Inspect raw customer, ticket, campaign, device, and status tables
* Check missing values and duplicates
* Standardize date and time fields
* Create cleaned CSV files
* Build the final joined dataset for analysis

### 2. Customer Profile Analysis

This section analyzes customer demographic information.

Main focus areas:

* Customer gender distribution
* Age distribution
* Customer profile quality
* Invalid or unusual date of birth values

This helps understand what types of customers are using the ticket booking platform.

### 3. Purchase Timing Analysis

This section explores when customers make purchases.

Main focus areas:

* Purchase hour
* Purchase day of week
* Purchase month
* Time-of-day behavior
* Platform usage by purchase time
* Payment method patterns

This analysis helps identify customer booking habits and potential peak transaction periods.

### 4. Customer Segment Analysis

This section explores customer behavior by platform, campaign type, and purchase value.

Main focus areas:

* Mobile vs website usage
* Campaign vs non-campaign transactions
* Payment method behavior
* Spending behavior based on final ticket price
* Customer grouping based on transaction patterns

This helps identify meaningful customer groups for business reporting and marketing decisions.

### 5. Customer Retention Analysis

This section focuses on customer journey and repeat purchase behavior.

Main focus areas:

* Sort transactions by customer and time
* Assign purchase sequence number for each customer
* Identify first purchase and repeat purchase behavior
* Separate customers into promotion and non-promotion groups
* Build cohort-style retention analysis
* Compare how many customers return after their first purchase

This analysis is important because it connects marketing campaigns with customer loyalty and long-term business value.

## Key Findings

Some key observations from the analysis include:

* The platform contains a large number of customer and ticket transaction records.
* Mobile appears to be an important platform for ticket purchases.
* Campaign usage can be separated into promotion and non-promotion groups.
* Customer purchase sequence can be used to study whether customers return after their first order.
* Cohort analysis helps show how customer retention changes month by month.
* The final joined dataset makes it easier to analyze customer behavior from multiple business angles.

## Power BI Dashboard

A Power BI dashboard can be added to summarize the main insights visually.

Suggested dashboard pages:

1. Executive Overview

   * Total transactions
   * Total customers
   * Successful orders
   * Total revenue
   * Average ticket value

2. Customer Profile

   * Gender distribution
   * Age distribution
   * Customer count by segment

3. Purchase Behavior

   * Orders by month
   * Orders by day of week
   * Orders by hour
   * Platform comparison
   * Payment method comparison

4. Campaign and Retention

   * Promotion vs non-promotion customers
   * Repeat purchase rate
   * Customer retention by cohort
   * Campaign type performance

Dashboard link:

```text
Add Power BI dashboard link here
```

Dashboard preview:

```text
Add dashboard screenshot here
```

## How to Run This Project

### 1. Clone the repository

```bash
git clone https://github.com/qtrung123/Online-Ticket-Booking-Data-Analysis-Customer-Retention-Study.git
```

### 2. Open the project folder

```bash
cd Online-Ticket-Booking-Data-Analysis-Customer-Retention-Study
```

### 3. Install required packages

```bash
pip install pandas matplotlib seaborn jupyter
```

### 4. Run the notebooks

Open Jupyter Notebook or VS Code and run the notebooks in this order:

```text
01_data_overview.ipynb
02_customer_profile.ipynb
03_purchase_timing.ipynb
04_customer_segments.ipynb
05_customer_journey.ipynb
```

## Skills Demonstrated

This project demonstrates the following data analyst skills:

* Data cleaning and preprocessing
* Handling multi-table datasets
* Joining relational data sources
* Exploratory data analysis
* Customer segmentation
* Cohort and retention analysis
* Business problem solving
* Data visualization
* Power BI dashboard planning
* GitHub project documentation

## What I Learned

Through this project, I practiced transforming raw business data into a structured analytical dataset and using it to answer practical business questions. I also learned how to analyze customer retention, compare promotion and non-promotion behavior, and organize a data project in a way that is easy for recruiters and hiring managers to review.

## Future Improvements

Potential improvements for this project include:

* Add a Power BI dashboard link
* Add dashboard screenshots to the README
* Create a `requirements.txt` file
* Add summary charts inside the README
* Calculate clear retention rate metrics for promotion vs non-promotion customers
* Add SQL queries for business reporting
* Create a short executive summary PDF for HR review


