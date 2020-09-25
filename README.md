# XML-parsing
from urllib import request
from bs4 import BeautifulSoup

url = input('Enter -')
web = request.urlopen(url).read()
soup = BeautifulSoup(web,'html.parser')
tags = soup('title')
for tag in tags:
      print('title-\n',tag.text)
      
