# Selenium_Setup

This module provides a function to set up a Selenium webdriver instance with customizable options. Includes options to use Chrome or Firefox.

## Prerequisites
Python 3.x
Selenium
webdriver-manager
Usage
Import the setup function from the module:
```
from selenium_setup import setup
```
Then, call the setup function with desired parameters.

The function has the following parameters:

- headless (default: True): Whether or not to run the browser in headless mode
- download_dir (default: None): The download directory to set for the browser instance
- browser (default: 'Chrome'): The browser to use (either 'Chrome' or 'Firefox')

The function returns a tuple with three values:

- The webdriver instance
- A WebDriverWait instance with an implicit wait of 5 seconds and ignored exceptions NoSuchElementException and StaleElementReferenceException
- An ActionChains instance

Example usage:

```
driver, wait, actions = setup(headless=True, download_dir='C:/Downloads')
driver.get('https://www.google.com')
search_box = driver.find_element_by_name('q')
search_box.send_keys('Hello, world!')
search_box.submit()
```
