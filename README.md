# Exno-2appds
**AIM:**
    
    To Perform Data Collection through web scraping using python.

**ALGORITHM:**
	Step 1: Include the Necessary python libraries.
 
	Step 2: Use the requests library to send HTTP requests to a web page.
 
	Step 3: Retrieve the HTML content and use BeautifulSoup to parse it.
 
	Step 4: Navigate and extract the necessary data.
 
	Step 5: Handle the Java script content and retrieve the data using the html tags.
 
	Step 6: Check with the website permission and scrap the content.

**CODING & OUTPUT:**
```
DEVELOPED BY: S.Haridharshini
REG NO: 212221230033
```
```
import requests
from bs4 import BeautifulSoup
import pandas as pd

url = 'https://www.geeksforgeeks.org/python-logical-operators/?ref=lbp'
response = requests.get(url)
response


soup = BeautifulSoup(response.content, 'html.parser')
headings = soup.find_all('h2')
headlist = [x.text for x in headings]
for heading in headlist:
   print(heading)

df=pd.DataFrame(headlist,columns=['Headings'])
df.to_csv('newdata.csv', index=False)
df
```
![Screenshot 2024-11-27 210415](https://github.com/user-attachments/assets/4fab45f3-e982-45d2-99d1-b6f39a337958)
![Screenshot 2024-11-27 210439](https://github.com/user-attachments/assets/9d1215ae-4ca8-4074-b7ab-bc6d7adf19be)
![Screenshot 2024-11-27 210502](https://github.com/user-attachments/assets/675ba01d-23ad-4a52-84f4-e8c04286a940)


**RESULT:**
Thus , data Collection through web scraping using python is successfully performed.


 
