# Amazon Price Tracker

## Overview
This project is a web scraping tool that tracks the price of a product on Amazon using its URL. It periodically checks the price over a specified timeframe and sends an email notification when the price drops below a defined threshold.

## Features
- Scrapes product price from Amazon using BeautifulSoup.
- Tracks price changes over time.
- Sends an email alert when the price falls below a specified value.

## Technologies Used
- Python
- BeautifulSoup (for web scraping)
- Requests (for making HTTP requests)
- smtplib (for sending email notifications)
- dotenv (for managing environment variables)

## Usage

1. Update the `config.py` file with your desired Amazon product URL and target price:
   ```python
   PRODUCT_URL = "https://www.amazon.com/dp/B09XYZ1234"
   TARGET_PRICE = 10.00
   ```
2. Run the script:
   ```sh
   python tracker.py
   ```

## How It Works
- The script fetches the product page and extracts the price using BeautifulSoup.
- It checks the price at regular intervals (can be scheduled using a cron job or task scheduler).
- If the price falls below the target price, an email notification is sent.

## Notes
- Amazon has strict scraping policies; excessive requests may lead to temporary IP bans.
- Consider using headers and user-agent rotation to avoid detection.
- This project is for educational purposes. Always comply with Amazon's Terms of Service.

## Author
[Tridha Mukherjee](https://github.com/TridhaMukherjee)

