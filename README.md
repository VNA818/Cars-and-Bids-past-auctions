# Cars-and-Bids-past-auctions

*CSV file containing information on all past auctions from Cars & Bids*

### Updated 5/3/2022

**(Updated Periodically)** 

Scraped from: https://carsandbids.com/past-auctions/ 

Scraped using: https://chrome.google.com/webstore/detail/web-scraper-free-web-scra/jnhgnonknehpejjnehehllkliplmbmhn?hl=en

[data.csv](./Data/data.csv) contains all past auctions from Cars & Bids as of updated date

## Format example

| Model | Description | Result | Date-Ended | Link |
| --- | --- | --- | --- | --- |
| 2009 Nissan 350Z Roadster | ~22,900 Miles, 306-hp V6, Touring Trim, Accident-Free Carfax Report | Sold for $16,500 | 7/9/2021 | https://carsandbids.com/auctions/3qYoEvMa/2009-nissan-350z-roadster |
| 2014 Ford Mustang GT Coupe | Final-Year S197, Extensive Modifications, New Mexico-Kept | Bid to $15,800 | 2/5/2021 | https://carsandbids.com/auctions/37QeDMER/2014-ford-mustang-gt-coupe |
| 2001 Ferrari 360 Modena | ~13,900 Miles, 20-Year Current Owner, Service History Since New | Bid to $74,000 (Sold After) | 6/30/2021 | https://carsandbids.com/auctions/KPJBavq2/2001-ferrari-360-modena |
| 1994 Pontiac Firebird Trans Am SLP Firehawk | ~6,200 Miles, 1 Owner Until 2021, 6-Speed Manual, Supercharged V8 Power | Cancelled | 3/2/2022 | https://carsandbids.com/auctions/KP8Qyqd2/1994-pontiac-firebird-trans-am-slp-firehawk |

## Scraping Instructions

1. Install above Chrome extension
2. Navigate to above Cars & Bids link
3. Go into developer tools in your browser & click on the "Web Scraper" tab
4. Click on "Create new sitemap" -> "Import sitemap" and paste in the json from [sitemap.json](./Scraper/sitemap.json)
5. Select the sitemap and click "Sitemap carsandbids" -> "Scrape" -> "Start scraping" 

**Note: The Cars & Bids website must be fully zoomed out to show all cars on each page or else the listings will lazy load and the scraper will not work**

6. When finished click on "Sitemap carsandbids" -> "Export data" -> ".CSV"
7. Edit the CSV file to conform to the above format (Delete first two columns, remove "Ended" from dates, add https://carsandbids.com/ to links)
