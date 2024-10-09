## List-Of-Companies- Webscrapper Project

### Table of Contents
- [Project Overview](#project-overview)
- [Data Source](#data-source)
- [Python Tools](#python-tools)
- [Execution and Steps](#execution-and-steps)
- [Conclusion and Recommendation](#conclusion-and-recommendation)
- [References](#references)

### Project Overview
---
This is a simple python web scrapping project that seeks to demonstrate clear procedures to get html data(tables) from websites and web pages of organisations who permit this process. The html tags were identified with their headers, cleaned and read with pandas dataframe to give it a better table structure before exporting as a CSV file. This also helps data scientists and analyst to search for original data themselves.

### Data Source
The data was scrapped from wikipedia as the "List of largest companies by revenue/Publickly traded companies in the US for the 2023 Fiscal Year.

### Python Tools
- Requests library: For creating response request to the web page
- BeautifulSoup: For finding and getting all html tags and data
- Pandas:Creating rows and columns storing in a dataframe
### Execution and Steps
The following actions and steps were executed on this web scrapping exercise:
1. Importing all libraries and packages
   ```Python
   import requests
   from bs4 import BeautifulSoup
   import pandas as pd
   ```
3. creating a url variable of the web page
   ```python
   url= 'https://en.wikipedia.org/wiki/List_of_largest_companies_in_the_United_States_by_revenue'
   ```
5. creating response request and getting html tags and data using appropriate python syntax
   ```python
   page = requests.get(url)
   ```
7. Identifying and sorting the html tags with specified tables needed
   ```python
   soup = BeautifulSoup(page.text, 'html.parser')
   ```
9. Cleaning and storing scrapped table in a pandas dataframe
  ```python
  df=pd.DataFrame(columns=world_table_tiltes)
  df
  ```
11. Exporting pandas data as a csv file into specified directory.
   ```python
   df.to_csv(r'C:\Users\HP ELITEBOOK 840 G3\Desktop\Mandy programs/company.csv', index=False)
   ```
### Conclusion and Recommendation
Though web scrapping is not a practice widely accepted and allowed for all websites and pages, it can be a poweful skillset to pull out data without having to depend on other sources or personell for a dataset. By mastering the usage of these libraries and some coding syntax this process can be done seemlessly especially if permission is granted by a webpage. Check out for full python syntax for this project and exercise.

### References
- [WIKIPEDIA](https://en.wikipedia.org/wiki/List_of_largest_companies_in_the_United_States_by_revenue)
- [PYTHON](https://www.python.org/)




