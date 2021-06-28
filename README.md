Flipkart-Webscraping
Webscraping the datas of Macbooks from Flipkart.com

What is Web Scraping?

Web scraping, also known as web data extraction, is the process of retrieving or “scraping” data from a website. This information is collected and then exported into a format that is more useful for the user and it can be a spreadsheet or an API. Although web scraping can be done manually, in most cases, automated tools are preferred when scraping web data as they can be less costly and work at a faster rate.

Libraries used for Web Scraping:

BeautifulSoup: BeautifulSoup is a Python library for pulling data out of HTML and XML files. It works with your favourite parser to provide idiomatic ways of navigating, searching, and modifying the parse tree.

Pandas: Pandas is a fast, powerful, flexible, and easy to use open-source data analysis and manipulation tool, built on top of the Python programming language.

Why BeautifulSoup? It is an incredible tool for pulling out information from a webpage. You can use it to extract tables, lists, paragraphs and you can also put filters to extract information from web pages.

Scraping Flipkart Website:

from bs4 import BeautifulSoup import requests import csv import pandas as pd

First, we import the BeautifulSoup and the requests library and these are very important libraries for web scraping.

requests: requests, is one of the packages in Python that made the language interesting. requests is based on Python’s urllib2 module.

Datas extracted are:

Name of the product
Price
Certificate
Reviews
Ratings
Features
Extracting the descriptions:

When you click on the “Inspect” tab, you will see a “Browser Inspector Box” open.We use the find method to extract the descriptions of the laptops.

Create an empty list to store the descriptions of all the laptops. We can even access the child tags with dot access. So now iterate through all the tags and then use the .text method to extract only the text content from the tags. In every iteration append the text to the descriptions list. So after iterating through all the tags, the descriptions list will have the text content of all the Macbooks (which is the description of the Macbook-model name along with specifications). Similarly, we apply the same approach to extract all the other features.

Final step:

Merge all the features into a single data frame and store the data in the required format
