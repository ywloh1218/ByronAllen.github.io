---
layout: post
title: Scraping Seek.com.au!
---
As part of the projects I completed at DSI2, I built a webscraper that took >1000 data science job postings from Seek.com.au and parsed them for salary information.

First, here are the modules I'm starting with.
![_config.yml]({{ site.baseurl }}/images/P4mods.png)

Adapting a function from Greg Reda at [gregreda.com](http://www.gregreda.com/2013/03/03/web-scraping-101-with-python), and using the 'requests' module to obtain the HTML from the page, (And of course, parsing the HTML with BeautifulSoup), I wrote a function to parse through Seek pages and develop a list of job posting links.

![_config.yml]({{ site.baseurl }}/images/ScrapFunc.png)

Applying the function to Seek's search results for the term "Data",

![_config.yml]({{ site.baseurl }}/images/1stScrape.png)

And there we go! We've scraped the first page of Seek, obtaining 20 links. We need 1000 links, so I'm going to write another function to "turn the page" for me.

Looking at the URLs for each Seek page,
![_config.yml]({{ site.baseurl }}/images/URL_list.png)
We can see that each page is similar to the page before it, with the only difference being X, where page=X. Now we can write the full function to scrape Seek.com.au and get all job links!

![_config.yml]({{ site.baseurl }}/images/FullScrape.png)



Click [here](https://github.com/ywloh1218/DSI_Project4/blob/master/yenP4_scrapeNclean.ipynb) to see the full notebook.
