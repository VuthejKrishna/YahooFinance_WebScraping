# YahooFinance_WebScraping

The Stock Market Exchange Database

2019 Version
Release Date: December 08, 2019

----------------------------------------------------------------------------------------------------------------------

Introduction to Yahoo Finance:

Yahoo Finance is a media property that is part of Yahoo's Network.
It provides Financial News, Data and Commentary including Stock Quotes, 
Press Releases, Financial Reports and Original Content.
It is the largest business news website in the United States by Monthly traffic.

License Information:

Licensed under © 2019 Verizon Media.

Copyright © 2018 Refinitiv. Refinitiv content is the intellectual property of Refinitv. 
Any copying, republication or redistribution of Refinitv content, including by caching, framing or similar means,
is expressly prohibited without the prior written consent of Refinitiv. 
Data is provided for information purposes only and is not intended for trading purposes. 
Refinitiv is not liable for any errors or delays in content, or for any actions taken in reliance on any content. 
Refinitiv and the Refinitiv Logo are trademarks and registered trademarks of the Refinitiv companies around the world.

For details, see: https://help.yahoo.com/kb/finance-for-web/SLN2310.html?impressions=true

----------------------------------------------------------------------------------------------------------------------

README CONTENTS

1.1 Introduction
1.2 Description
1.3 Challenges Faced
1.4 Conclusion/Future Work
1.5 Acknowledgements

2.0 YahooFinance_WebScraping.ipynb
2.1 CSV Files
2.2 JSON Files
2.3 Accenture
2.4 Adobe INC
2.5 Advanced Microdevices
2.6 Amphenol Corporation
2.7 Analog Devices INC
2.8 Apple
2.9 Applied Materials
2.10 ASML
2.11 Atlassian Corporation Plc
2.12 Autodesk Inc
2.13 Broadcom Inc
2.14 Canon Inc
2.15 Cisco Systems
2.16 Cognizant Technology Solutions Corporation
2.17 DELL
2.18 Fidelity National Information Services
2.19 FleetCor Technologies Inc
2.20 Fortive Corporation 1
2.21 Fortive Corporation 
2.22 HP Inc
2.23 IBM
2.24 Infosys Limited
2.25 Intel Corporation
2.26 Intuit Inc
2.27 KLA Corporation
2.28 Lam Research Corporation
2.29 Microchip Technology ---
2.30 Micron Technology
2.31 Microsoft Corporation
2.32 Motorola Solutions, Inc
2.33 NVIDIA
2.34 NXP Semiconductors
2.35 Oracle Corporation
2.36 QUALCOMM Incorporated
2.37 Salesforce
2.38 SAP
2.39 ServiceNow
2.40 Shopify Inc
2.41 Sony Corporation
2.42 Splunk Inc
2.43 Square Inc
2.44 ST Microelectronics NV
2.45 Taiwan_Semiconductor_Manufacturing_Company_Limited
2.46 TE Connectivity Ltd
2.47 Telefonaktiebolaget LM Ericsson
2.48 Texas Instruments Incorporated
2.49 Uber Technologies
2.50 VMware
2.51 Workday Inc
2.52 Xilinx Inc

----------------------------------------------------------------------------------------------------------------------

1.1 Introduction

Yahoo! Finance is a media property that is part of Yahoo!'s network. 
It provides financial news, data and commentary including stock quotes, 
press releases, financial reports, and original content. 
It also offers some online tools for personal finance management. 
In addition to posting partner content from a wide range of other web sites,
it posts original stories by its team of staff journalists.

As of June 2017, Yahoo Finance is part of Oath, the media division of Verizon. 
It is the largest business news web site in the United States by monthly traffic.

----------------------------------------------------------------------------------------------------------------------

1.2 Description

Data Harvesting performed on the Yahoo Finance website https://finance.yahoo.com/ to extract data like..

History of share market for the TOP 50 companies in Technological Domain.
Attributes include 'Date', 'Open', 'High', 'Low', 'Close', 'Adj Close', 'Volume'.

Apart from this, other attributes have also been harvested.
'Sector', 'Industry', 'Full Time Employees', 'Name', 'Title', 'Pay', 'Exercised', 'Year Born',
'Enterprise Value', 'Quarterly Growth', 'Forward P/E', 'PEG Ratio (5 years expected)',
'Return on Assets', 'Quarterly Revenue Growth', 'EBITDA', 'Diluted EPS', 'Total Debt or Equity', 'Current Ratio'.

----------------------------------------------------------------------------------------------------------------------

1.3 Challenges Faced and Overcomed

In the initial stages of our project, we had several options to consider for data harvesting like NYSE, NASDAQ, Yahoo Finance.
Based on the terms and conditions of each website, it has been decided to proceed with Yahoo Finance.

As the Yahoo Finance website was having a varied structure for different attributes, extraction had a level of complexity involved in it.
In order to overcome this, we had to perform multilevel extractions for building the structure.

Explicit links had to be created in the code for extracting data from the specific company hyperlinks instead of going to the hyperlinks directly.
To overcome this, we considered the initial link that landed us on the home page of Yahoo Finance and then html links were built specific to the company by using
company's share mnemonic.

Few instances of the extracted data has special characters which when stored and built in an excel sheet, it appears to be a special character.
This further needs additional cleaning in order to remove the special characters.

There were null values for few attributes which were company specific. For instance, a multi-layered dictionary was having null values for internal keys and 
this caused hindrance in creating the structured data. It took some efforts in finding out the companies to which this issue was specific to.
In order to overcome this, decision structure has been included to consider and have them populated with the N/A.


----------------------------------------------------------------------------------------------------------------------

1.4 Conclusion/Future Work

Further attributes can be included in order to enrich the data set which helps in better evaluating and analyzing at the later stage.
Along with additional attributes, additional instances of data can also be added by expanding the scope to other companies.

This can also be integrated with other projects trying to check the stock market price or for projects implementing any specific company details for their project.

----------------------------------------------------------------------------------------------------------------------

1.5 Acknowledgements

All of the data from this work comes from the Yahoo Finance website.

We thank our instructor Heejun Kim for sharing the knowledge and supporting us in completing this project.

----------------------------------------------------------------------------------------------------------------------

2.0 YahooFinance_WebScraping.ipynb

This is the jupyter notebook where we have all our code along with the description of what the code in each cell does.

----------------------------------------------------------------------------------------------------------------------

2.1 CSV Files


Stock_Market_Attributes.csv and Statistics.csv provides the data of TOP 50 Technological companies with below fields as columns.
Third file which is generalized as <company.csv> is a broad classification of various other files. (One for each company's 5 years data)

Stock_Market_Attributes.csv

'Sector'			- This field details the area within the domain that the company is interested in
'Industry'			- This field describes the domain to which the company belongs to
'Full Time Employees'		- Count of all the employees in the company
'Name'				- 5 Names of high-level executives (CEO, COO, Director, President, Vice President,
			  	  Chief Financial Officer, Chairman, MD, General Manager, CTO and so on..)
'Title'				- Corresponding job roles/designations for executives presented under 'Name' column
'Pay'				- Corresponding pay received by executives mentioned under 'Name' column
'Exercised'			- Shares of the stock that have been purchased per the stock option agreement
'Year Born'			- Birth Year of the executives mentioned under 'Name' column.

Statistics.csv

'Enterprise Value'		- Economic measure reflecting the market value of the business
'Quarterly Growth'		- It is an increase in a company's sales in one quarter compared to sales of previous quarter
'Forward P/E'			- P/E ratio is a current stock's price over "predicted" earnings per share
'PEG Ratio (5 years expected)'	- It is a valuation metric for determining relative trade off between the price of a stock,
				  the earnings generated per share and the company's expected growth
'Return on Assets'		- Percentage of profit a company earns. Net income divided by total assets
'Quarterly Revenue Growth'	- It is an increase in a company's sales in one quarter compared to sales of another quarter
'EBITDA'			- Earnings before interest, tax, depreciation and amortization
'Diluted EPS'			- It is a calculation used to gauge the quality of a company's earnings per share (EPS)
				  if all convertible securities were exercised
'Total Debt or Equity'		- Is the ratio of a company's total liabilities by it's shareholder equity
'Current Ratio'			- Comparison of firms current assets to it's current liabilities

<company.csv>

'Date'				- This depicts the date for which the stock market data is obtained for
'Open'				- Opening value of the share for that particular day
'High'				- Highest value that the share has reached for that particular day
'Low'				- Lowest value that the share has reached for that particular day
'Close'				- Value at the closing time of the day
'Adj Close'			- Adjusted Value at the end of the day
'Volume'			- Total Amount contributed by all the transactions accounting for a particular company on a given day 

----------------------------------------------------------------------------------------------------------------------

2.2 JSON Files

'Stock Market Attributes.json' and 'Statistics.json' files provide the dictionary structure of the data that has been scraped from Yahoo Finance.
These files consists of multi-layered dictionaries.

----------------------------------------------------------------------------------------------------------------------

2.3 to 2.53 Talks about all the <company>.csv files with 'Date', 'Open', 'High', 'Low', 'Close', 'Adj Close', 'Volume' attributes spanning over last 5 years.


<end of file>



