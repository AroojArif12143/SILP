# Web Scraping about Flood in Pakistan 
![pakistan-flood](https://user-images.githubusercontent.com/93564920/210174170-be372795-2243-4f36-bbcb-196cbc712f14.jpg)

In this tutorial, we will be learning how to perform **web scraping** via Python to gather news about Flood in Pakistan easily. **Web Scraping** is the procedure gathering and converting raw data on the internet. Web scraping is a good alternative to assist us in collecting the required data easily if we are unable to find readily available data online. 

Firstly, let us pip install gnews if it is not installed by running the below command. Gnews is a python package that allow us to search article on Google News and return with a JSON response. 
```
!pip install gnews
```
After install the gnews package, we can import the necessary libraries.
```
# import libraries 
import pandas as pd 
from gnews import GNews
```
After importing the gnews package, let us create the Google News API with the parameters. In our tutorial, we set the language and country as *jp*. You can also set other language and country that are supported.
```
# create the Google News API with parameters 
google_news = GNews(language='jp', country='JP')
```
Then, we can create the search by calling **.get_news** with the search parameter that we are looking to find. In this example, we will be searching for **自然災害** *(which is natural disaster in chinese)* and store it in the *natural_disaster* variable.
```
# let's create the search 
natural_disaster = google_news.get_news('自然災害')
```
Let us take a look at the title for the news that we search. 
```
# Lets loop through the actual titles 
for i in natural_disaster:
  print(i['title'])
```
![Gnews Title](picture/gnews_title.png)

For ease of handling the data, let us convert it to dataframe by using Pandas. After converting it to dataframe, let us have a preview of what data we have. 
```
# Convert the JSON into dataframe 
data = pd.DataFrame(natural_disaster)
data.head()
```
![Gnews Preview](picture/gnews_preview.png)


Kudos, you made it to the end of the tutorial. Well Done!:star2:

