# Amazon Web Scrapping (Price Tracker)

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
   PRODUCT_URL = "(https://www.amazon.com/Never-Forget-Shirt-Science-T-Shirt/dp/B07WQ5QB83/ref=sr_1_16?crid=MJ75HSDLOK9L&customId=B0752XJYNL&customizationToken=MC_Assembly_1%23B0752XJYNL&dib=eyJ2IjoiMSJ9.o60EHLqu5DeAmm2A0l89BOEjNPx043zUdNZz3Fw_b1IpqJ-Gzvpx71l5pAaeut8ykTnT6-iu3UQRrdHhxynO9t7MB0IvaHx7vvyNuCyaGbfTlGiJHuOpm_rxi_np0_kf0RvNzEQmelYTZ4HVNHU_AuLQKMeSPfXTQ5cYZmQI60qpfr3SiNetyFnQyC9ZfSZDDYG_JWCeY8WV1OwCfP1olULAV3r1uiGu__y4Attao18uZBci1HJVq7IoESt4I1K5cpLuutLIrjNZ7UFLlD5UMykmOyEWmjbrHKLJ_qa1kHg.SyczVKDNOVuZvvpjKbSMM7G9p3hlQON2yE4bWDpPKy0&dib_tag=se&keywords=tshirts+shirts+for+men+graphic&qid=1710273606&sprefix=tshirts+shirts+for+men+%2Caps%2C126&sr=8-16)"
   TARGET_PRICE = 10.00
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

