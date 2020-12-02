# Web Scrapping
*Web scraping is a technique to automatically access and extract large amounts of information from a website*

### Import Libraries
```
import requests
import urllib.request
import time
from bs4 import BeautifulSoup
```
### Find Links
use **Inspect** tool to examine website and locate URL for data
### Access URL
```
url = 'http://web.mta.info/developers/turnstile.html'
response = requests.get(url)
```
### Clean it up
```
soup = BeautifulSoup(response.text, “html.parser”)
```
### Find anchor tags
```
soup.findAll('a')
```
### Locate a Tag
```
one_a_tag = soup.findAll(‘a’)[38]
link = one_a_tag[‘href’]
```
### use urllib.request to download
```
download_url = 'http://web.mta.info/developers/'+ link
urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:])
```
### Include a pause
```
time.sleep(1)
```
### Grab all by looping
```
# Import libraries
import requests
import urllib.request
import time
from bs4 import BeautifulSoup

# Set the URL you want to webscrape from
url = 'http://web.mta.info/developers/turnstile.html'

# Connect to the URL
response = requests.get(url)

# Parse HTML and save to BeautifulSoup object¶
soup = BeautifulSoup(response.text, "html.parser")

# To download the whole data set, let's do a for loop through all a tags
line_count = 1 #variable to track what line you are on
for one_a_tag in soup.findAll('a'):  #'a' tags are for links
    if line_count >= 36: #code for text files starts at line 36
        link = one_a_tag['href']
        download_url = 'http://web.mta.info/developers/'+ link
        urllib.request.urlretrieve(download_url,'./'+link[link.find('/turnstile_')+1:]) 
        time.sleep(1) #pause the code for a sec
    #add 1 for next line
    line_count +=1
```
