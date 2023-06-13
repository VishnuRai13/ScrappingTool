import requests
from bs4 import BeautifulSoup

# Prompt the user to enter the URL of the website to scrape
url = input("Enter the URL of the website to scrape: ")

# Send a GET request to the URL
response = requests.get(url)

# Create a BeautifulSoup object to parse the HTML content
soup = BeautifulSoup(response.content, 'html.parser')

# Find and extract specific elements from the HTML
# Customize these lines based on the structure of the website you're scraping
titles = soup.find_all('h2')  # Extract all <h2> elements

# Print the extracted data
for title in titles:
    print(title.text)

With this script, when you run it in the terminal, it will prompt you to enter the URL of the website you want to scrape. After entering the URL, the script will send a GET request to that URL, extract the desired data using BeautifulSoup, and print the extracted data.

Save the script to a file (e.g., scrape.py) and run it with python scrape.py in the terminal. You will be prompted to enter the URL at runtime.

