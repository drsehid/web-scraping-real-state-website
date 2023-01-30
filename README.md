# web-scraping-real-state-website

This is a Python code that uses web scraping to extract real estate data from Divar.ir website, performs data wrangling and pre-processing, and finally creates a model to predict the price of a house.

The code is divided into three main steps:
1. Extract Data from the Web and Save into a CSV File
2. Load CSV Data and Perform Data Wrangling
3. Create Model

1. Extract Data from the Web and Save into a CSV File
- This step involves web scraping of the Divar.ir website to extract real estate data.

**Required Libraries and Tools**
- Selenium: A tool to automate the browser actions required to scrape the website.
- BeautifulSoup: A Python library to parse HTML and XML pages.
- webdriver_manager: A library that helps to manage the downloading and installation of the web drivers required by Selenium.

**Functionalities**
- Installing the appropriate version of ChromeDriver by using the ChromeDriverManager class from the `webdriver_manager` package.
- Scrolling down the pages of the website using Selenium WebDriver and extracting the source text using `BeautifulSoup`.
- Finding all the links in a page using the `BeautifulSoup.findAll()` method, filtered by a specific class.
- Opening each link using the `requests` library, parsing the page content and creating a `BeautifulSoup` object for each page.
- Finding all the HTML tags that have relevant data for our purpose, using the `BeautifulSoup.findAll()` method, filtered by specific class names.
- Storing each real estate data in a list, as a tuple.
- Saving the list of tuples into a `DataFrame` object using the `pandas` library.

2. Load CSV Data and Perform Data Wrangling
- In this step, the data saved in the CSV file from the previous step is loaded and pre-processed.

**Required Libraries and Tools**
- pandas: A library used to load the CSV data and perform data wrangling.

**Functionalities**
- Loading the data saved in the CSV file into a `DataFrame` object using the `pandas.read_csv()` method.
- Cleaning the data in the `DataFrame` by removing the missing or duplicate values, and converting the data into the correct data types.

3. Create Model
- In this step, the cleaned and pre-processed data from the previous step is used to create a model.

**Required Libraries and Tools**
- numpy: A library used for numerical computations and data manipulation.
- matplotlib: A library used for data visualization.
- re: A library used for pattern matching.
- seaborn: A library used for creating visualizations for statistical models.

**Functionalities**
- Plotting a scatter matrix of the data to visualize the relationships between different variables.
- Creating a model to predict the price of a house, using the cleaned and pre-processed data.
