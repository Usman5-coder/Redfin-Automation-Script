# 🏡 Redfin Property Link Extractor – Documentation

## 📖 Overview

**Redfin Property Link Extractor** is a powerful and user-friendly Python script designed to automate the extraction of property listing links from [Redfin.com](https://www.redfin.com).  
By guiding users through a city-specific search, this tool fetches filtered property links and organizes them into a well-formatted Word document—all through a seamless command-line interface.

Whether you're a data analyst, real estate researcher, or an automation enthusiast, this script simplifies repetitive browsing tasks and helps you gather property data with minimal effort.

---

## 🚀 Features & Workflow

### 1. 🔗 Website Initialization
- Launches an automated browser session using **Selenium WebDriver**
- Navigates to: `https://www.redfin.com`
- Prepares the environment for user interaction and automated navigation

### 2. 🏙️ User Input – City Selection
- CLI prompt:  
  `Enter the name of the city you'd like to search properties in:`
- Accepts dynamic input (e.g., *San Francisco*, *Austin*, *Miami*)
- Personalized city search support

### 3. 🔍 Intelligent Search & Load Handling
- Inputs the city into Redfin’s search bar
- Waits for auto-suggestions and navigates to the correct city
- Uses **WebDriverWait** and DOM checks to ensure page is fully loaded

### 4. 🎯 Applying Filters
Applies essential filters:
- Property Type
- Price Range
- Status: *For Sale*
- Bedrooms/Bathrooms
- Comps sold in last 12 months with price $200K+

Uses Selenium selectors to apply filters and waits for the result page to fully load.

### 5. 🕸️ Web Scraping – Extracting Property Links
- Dynamically scrolls the page to load lazy-loaded listings
- Extracts property links from `<a>` tags inside listing containers
- Filters duplicates and malformed URLs
- Stores results in a Python list

### 6. 📝 Documenting Results
- Generates a structured Word document (`addresses.docx`)
- Each link added as a numbered, clickable item
- CLI confirmation message:


### 7. ⚠️ Error Handling & Logging
- Wrapped critical operations in `try/except` blocks
- Provides descriptive CLI error messages
- Ensures graceful failure if Redfin layout changes or ChromeDriver errors occur

---

## 📌 Notes

- Ensure **Google Chrome** and the correct **ChromeDriver** version are installed
- Adjust filter selectors if Redfin changes its layout or class names
- Running the script in a **virtual environment** is recommended

---

## 📝 Usage Notes for Redfin Scraper

- Use cities in this format: `City, State` (e.g., `San Francisco, CA`)
- Major metro areas are prioritized for best results
- Smaller regional centers also supported

---

## 🎯 Recommended High-Activity Markets

**California**
- Los Angeles
- San Francisco
- San Diego
- San Jose

**Texas**
- Houston
- Dallas
- Austin
- San Antonio

**Florida**
- Miami
- Tampa
- Orlando
- Jacksonville

**New York**
- New York City
- Buffalo
- Rochester

**North Carolina**
- Charlotte
- Raleigh
- Durham
- Wake Forest

---

## ✅ Final Output Example

A generated Word document (`addresses.docx`) will look like:


---

## 👨‍💻 Author

**Muhammad Usman Subhani**  
[GitHub](https://github.com/your-username) · [LinkedIn](https://linkedin.com/in/your-profile) · [Twitter](https://twitter.com/your-handle)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---
