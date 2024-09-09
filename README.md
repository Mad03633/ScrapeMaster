# Scrape Master

Scrape Master is a web application built using Streamlit that allow users to scrape and extract meaningful information from websites. It utilizes Selenium for web scraping, BeautifulSoup for parsing HTML content, and the LangChain framework integrated with the OllamaLLM model for advanced parsing of DOM content based on user-provided descriptions.

## Features

- **Website scraping**: Scrape website DOM content with the help of Selenium.
- **Content Extration**: Extract and clean body content using BeatifulSoup.
- **Custom Parsing**: Parse the scraped content based on user-defined descriptions using LangChain and the Ollama model.
- **Captcha Handling**: Automatically waits and handles CAPTCHA during scraping.
- **Streamlit UI**: Interactive and easy-to-use web interface.

## Requirements

Ensure you have the following dependencies installed:
- streamlit
- selenium
- beatifulsoup4
- langchain
- ollama

## How it Works

1. **Scraping**: The app uses Selenium WebDriver to scrape the content of the provided website URL. CAPTCHA solving is handled during the scraping process.
2. **Content Extraction**: After scraping the website, the body content of the webpage is extracted and cleaned from unnecessary tags such as ```<script>``` and ```<style>``` using BeautifulSoup.
3. **Content Parsing**: The cleaned content is split into smaller chunks and passed to the ```parse_with_ollama``` function, which uses the LangChain framework and OllamaLLM to extract specific information based on the description provided by the user.

## Configuration

Make sure to update the ```SBR_WEBDRIVER``` variable with the correct path to your Chrome WebDriver in the ```scrape_website.py``` file.
```SBR_WEBDRIVER = 'path_to_chromedriver'```