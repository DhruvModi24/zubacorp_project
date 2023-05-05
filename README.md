# zubacorp_project

This project able to Scrape details of all companies listed for different “Status” types, like Active, striked-off,
under process of strike off from the 'https://www.zaubacorp.com/company-list-company.html' and store them in a MongoDB collection.

technologies you used:  [python, scrapy, mongodb, xpath]

Some of the challenges faced:

-There is 399990 companies listed if we are going threw pagination link. total pages are 13333.every page has 30 companies listed.
-There is a limition of pages.
-I analyse all filters so i found we have to go threw all filter with handle duplicate urls and geting the maximum result.

code flow:

-I go threw exract all pagenation link threw filter and insert all link in collection with flag.
-hit pagination link for data crawling and insert all data in data collection and update flag.

How to Install and Run the Project:

install requirment.txt

-Run first link spider to collect all page_links and dump link in collection [command] = scrapy crawl link_spider
-Run data spider to collect all data from page_link and dump data in collection [command] = scrapy crawl data_spider
