# zubacorp_project

This project able to Scrape details of all companies listed for different “Status” types, like Active, striked-off,
under process of strike off from the 'https://www.zaubacorp.com/company-list-company.html' and store them in a MongoDB collection.

technologies you used:  [python, scrapy, mongodb, xpath]

code flow:

-exract all pagenation link and insert all link in collection with flag.
-hit pagination link for data crawling and insert all data in data collection and update flag.

How to Install and Run the Project

install requirment.txt

-Run first link spider to collect all page_links and dump link in collection [command] = scrapy crawl link_spider
-Run data spider to collect all data from page_link and dump data in collection [command] = scrapy crawl data_spider
