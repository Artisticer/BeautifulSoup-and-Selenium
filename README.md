# BeautifulSoup-and-Selenium
Scrape dynamic web pages using both BeautifulSoup and Selenium.
from bs4 import BeautifulSoup
from selenium import webdriver

url = 'https://example.com'
driver = webdriver.Chrome('chromedriver.exe')  # Provide the path to your ChromeDriver executable
driver.get(url)

# Use Selenium to interact with dynamic content
dynamic_content = driver.find_element_by_css_selector('.dynamic-content').get_attribute('innerHTML')

# Use BeautifulSoup for parsing
soup = BeautifulSoup(dynamic_content, 'html.parser')
# Perform scraping tasks

driver.quit()
