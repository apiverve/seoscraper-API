SEO Data Scraper API
============

SEO Scraper is a simple tool for scraping SEO data. It returns the meta title, meta description, and more.

![Build Status](https://img.shields.io/badge/build-passing-green)
![Code Climate](https://img.shields.io/badge/maintainability-B-purple)
![Prod Ready](https://img.shields.io/badge/production-ready-blue)

This is a Javascript Wrapper for the [SEO Data Scraper API](https://apiverve.com/marketplace/api/seoscraper)

---

## Installation
	npm install @apiverve/seoscraper --save

---

## Configuration

Before using the seoscraper API client, you have to setup your account and obtain your API Key.  
You can get it by signing up at [https://apiverve.com](https://apiverve.com)

---

## Usage

The SEO Data Scraper API documentation is found here: [https://docs.apiverve.com/api/seoscraper](https://docs.apiverve.com/api/seoscraper).  
You can find parameters, example responses, and status codes documented here.

### Setup

```
var seoscraperAPI = require('@apiverve/seoscraper');
var api = new seoscraperAPI({
    api_key: [YOUR_API_KEY],
    secure: true //(Optional, defaults to true)
});
```

---


### Perform Request
Using the API client, you can perform requests to the API.

###### Define Query

```
var query = {
  "url": "https://ebay.com"
};
```

###### Simple Request (using Callback)

```
api.execute(query, function (error, data) {
    if (error) {
        return console.error(error);
    } else {
        console.log(data);
    }
});
```

###### Example Response

```
{
  "status": "ok",
  "error": null,
  "data": {
    "requestUrl": "https://ebay.com",
    "url": "https://www.ebay.com/",
    "canonical": "https://www.ebay.com",
    "lang": "en",
    "charset": "utf-8",
    "title": "Electronics, Cars, Fashion, Collectibles & More | eBay",
    "image": "",
    "favicons": [
      {
        "rel": "icon",
        "href": "https://pages.ebay.com/favicon.ico"
      }
    ],
    "author": "",
    "description": "Buy & sell electronics, cars, clothes, collectibles & more on eBay, the world's online marketplace. Top brands, low prices & free shipping on many items.",
    "keywords": "",
    "source": "",
    "price": "",
    "priceCurrency": "",
    "availability": "",
    "robots": "",
    "jsonld": [
      {
        "@context": "https://schema.org",
        "@type": "WebPage",
        "@id": "https://www.ebay.com/#webpage",
        "url": "https://www.ebay.com",
        "author": {
          "@type": "Corporation",
          "@id": "https://www.ebay.com/#corporation",
          "url": "https://www.ebay.com",
          "logo": "https://ir.ebaystatic.com/rs/v/fxxj3ttftm5ltcqnto1o4baovyl.png",
          "description": "eBay Inc. is an American multinational e-commerce corporation based in San Jose, California, that facilitates consumer-to-consumer and business-to-consumer sales through its website. eBay was founded by Pierre Omidyar in the autumn of 1995, and became a notable success story of the dot-com bubble. eBay is a multibillion-dollar business with operations in about 30 countries, as of 2011. The company manages the eBay website, an online auction and shopping website in which people and businesses buy and sell a wide variety of goods and services worldwide. The website is free to use for buyers, but sellers are charged fees for listing items after a limited number of free listings, and again when those items are sold.",
          "founder": {
            "@type": "Person",
            "@id": "https://www.ebay.com/#founder",
            "name": "Pierre Omidyar"
          },
          "foundingDate": "1995-09-03",
          "foundingLocation": "San Jose, CA",
          "name": "eBay",
          "legalName": "eBay Inc.",
          "contactPoint": {
            "@type": "ContactPoint",
            "availableLanguage": [
              {
                "@type": "Language",
                "name": "English",
                "alternateName": "en"
              },
              {
                "@type": "Language",
                "name": "Spanish",
                "alternateName": "es"
              }
            ],
            "contactOption": "TollFree",
            "contactType": "Customer Service",
            "telephone": "+1-866-961-9253"
          }
        },
        "isPartOf": {
          "@type": "WebSite",
          "@id": "https://www.ebay.com/#website",
          "url": "https://www.ebay.com",
          "potentialAction": {
            "@type": "SearchAction",
            "target": "https://www.ebay.com/sch/i.html?_nkw={srch_str}&ssPageName=GSTL",
            "query-input": "required name=srch_str"
          }
        },
        "inLanguage": "EN",
        "sameAs": [
          "https://www.facebook.com/ebay/",
          "https://www.pinterest.com/ebay/",
          "https://twitter.com/eBay",
          "https://www.linkedin.com/company/ebay/",
          "https://www.youtube.com/ebay",
          "https://www.instagram.com/ebay/"
        ]
      }
    ],
    "og:url": "https://www.ebay.com",
    "og:locale": "",
    "og:locale:alternate": "",
    "og:title": "Electronics, Cars, Fashion, Collectibles & More | eBay",
    "og:type": "website",
    "og:description": "Buy & sell electronics, cars, clothes, collectibles & more on eBay, the world's online marketplace. Top brands, low prices & free shipping on many items.",
    "og:determiner": "",
    "og:site_name": "eBay",
    "og:image": "https://ir.ebaystatic.com/cr/v/c1/ebay-logo-1-1200x630-margin.png",
    "og:image:secure_url": "",
    "og:image:type": "",
    "og:image:width": "",
    "og:image:height": "",
    "twitter:title": "Electronics, Cars, Fashion, Collectibles & More | eBay",
    "twitter:description": "Buy & sell electronics, cars, clothes, collectibles & more on eBay, the world's online marketplace. Top brands, low prices & free shipping on many items.",
    "twitter:image": "https://ir.ebaystatic.com/cr/v/c1/ebay-logo-1-1200x1200-margin.png",
    "twitter:image:alt": "",
    "twitter:card": "summary",
    "twitter:site": "@eBay",
    "twitter:site:id": "",
    "twitter:url": "",
    "twitter:account_id": "",
    "twitter:creator": "",
    "twitter:creator:id": "",
    "twitter:player": "",
    "twitter:player:width": "",
    "twitter:player:height": "",
    "twitter:player:stream": "",
    "twitter:app:name:iphone": "",
    "twitter:app:id:iphone": "",
    "twitter:app:url:iphone": "",
    "twitter:app:name:ipad": "",
    "twitter:app:id:ipad": "",
    "twitter:app:url:ipad": "",
    "twitter:app:name:googleplay": "",
    "twitter:app:id:googleplay": "",
    "twitter:app:url:googleplay": "",
    "headings": [
      {
        "level": "h1",
        "text": "eBay Home"
      },
      {
        "level": "h2",
        "text": "Shop by category"
      },
      {
        "level": "h4",
        "text": "Parts & Accessories"
      },
      {
        "level": "h4",
        "text": "Vehicles"
      },
      {
        "level": "h4",
        "text": "Top Categories"
      },
      {
        "level": "h4",
        "text": "Additional Categories"
      },
      {
        "level": "h4",
        "text": "Top Categories"
      },
      {
        "level": "h4",
        "text": "Featured"
      },
      {
        "level": "h4",
        "text": "Top Categories"
      },
      {
        "level": "h4",
        "text": "Additional Categories"
      },
      {
        "level": "h4",
        "text": "Top Categories"
      },
      {
        "level": "h4",
        "text": "Additional Categories"
      },
      {
        "level": "h4",
        "text": "Top Categories"
      },
      {
        "level": "h4",
        "text": "Featured"
      },
      {
        "level": "h4",
        "text": "Top Categories"
      },
      {
        "level": "h4",
        "text": "Popular Topics"
      },
      {
        "level": "h4",
        "text": "Top Categories"
      },
      {
        "level": "h4",
        "text": "Additional Categories"
      },
      {
        "level": "h4",
        "text": "Top Categories"
      },
      {
        "level": "h4",
        "text": "Top Brands"
      },
      {
        "level": "h4",
        "text": "Shop eBay Refurbished Electronics"
      },
      {
        "level": "h4",
        "text": "Shop eBay Refurbished Home"
      },
      {
        "level": "h2",
        "text": "Up to 70% off yellow gold jewelry"
      },
      {
        "level": "h2",
        "text": "Trending in Sneakers"
      },
      {
        "level": "h3",
        "text": "⚡️⚡️Size 10 - Air Jordan 4 Retro White Thunder PREORDER ⚡️⚡️"
      },
      {
        "level": "h3",
        "text": "SIZE 12 | REEBOK x ALIENS BB 4000 II MIDS INSPIRED BY ALIENS ROMULUS | FAST SHIP"
      },
      {
        "level": "h3",
        "text": "Air Jordan 4 White Thunder Men's FQ8138-001 Black/White Size 8.5 - BRAND NEW"
      },
      {
        "level": "h3",
        "text": "Nigel Sylvester x Air Jordan 4 RM SP  ''Anthracite''  Black Men's  HF4334-004"
      },
      {
        "level": "h3",
        "text": "Size 10 - Jordan 4 Retro Mid Red Thunder"
      },
      {
        "level": "h3",
        "text": "adidas Handball Spezial Preloved Green Gum - IG6192 Men's Shoes"
      },
      {
        "level": "h3",
        "text": "🔥 NIKE Air Jordan 4 Retro White Thunder FQ8213-001 GS SIZE 6.5Y / 8W BRAND NEW"
      },
      {
        "level": "h3",
        "text": "Size 10 - Nike Air Foamposite Pro ben gordon 2016"
      },
      {
        "level": "h3",
        "text": "🔥 NIKE Air Jordan 4 Retro White Thunder FQ8213-001  GS SIZE 7Y NEW IN HAND 🔥"
      },
      {
        "level": "h3",
        "text": "Size 7 - Adidas Yeezy Boost 700 Analog 'EG7596' Men's"
      },
      {
        "level": "h2",
        "text": "Trending in Watches"
      },
      {
        "level": "h3",
        "text": "Rolex Day Date President Presidential 36mm 18k Yellow Gold 1803 Circa 1977 $20k"
      },
      {
        "level": "h3",
        "text": "Rolex Tudor 75190 Prince Date Submariner Mens Amazing Watch Box Papers Tag"
      },
      {
        "level": "h3",
        "text": "Blancpain Aqualung Fifty Fathoms 1000 Feet Diver Vintage Watch 37mm"
      },
      {
        "level": "h3",
        "text": "Tudor Pelagos 25500T Black Dial Date 42mm Mens Automatic Divers Wrist Watch"
      },
      {
        "level": "h3",
        "text": "Rolex Oyster Perpetual DateJust Rhodium Dial 36MM 116234 Watch #LW-13"
      },
      {
        "level": "h3",
        "text": "Cartier Santos Carree Ref 2961 Two Tone S. Steel / 18K Gold 30mm Automatic Watch"
      },
      {
        "level": "h3",
        "text": "HEUER AUTAVIA 2446 CHRONOGRAPH ALL STEEL FABULOUS ORIGINAL DIAL, NICE BEZEL RUNS"
      },
      {
        "level": "h3",
        "text": "Rolex Datejust Turn-O-Graph 116264 THUNDERBIRD Box Tags & Papers 2007 White 36mm"
      },
      {
        "level": "h3",
        "text": "OMEGA Seamaster Aqua Terra 150M 220.10.41.21.10.001 - w/Box, No Papers"
      },
      {
        "level": "h3",
        "text": "OMEGA Seamaster Diver 300M Blue Dial Steel Bracelet - 210.30.42.20.03.001"
      },
      {
        "level": "h2",
        "text": "Score these trending kicks"
      },
      {
        "level": "h3",
        "text": "A Ma Maniére x Jordan 3 While You Were Sleeping WMNS"
      },
      {
        "level": "h3",
        "text": "Jordan 4 Paris Olympics Wet Cement"
      },
      {
        "level": "h3",
        "text": "Jordan 4 Retro White Thunder"
      },
      {
        "level": "h3",
        "text": "Nike SB Dunk Low x THERE Skateboards"
      },
      {
        "level": "h3",
        "text": "Jordan 4 RMs"
      },
      {
        "level": "h3",
        "text": "Kobe 4 Protro Gold Medal 2024"
      },
      {
        "level": "h3",
        "text": "Kobe 4 Protro Girl Dad"
      },
      {
        "level": "h2",
        "text": "Trending in Refurbished"
      },
      {
        "level": "h3",
        "text": "iRobot Roomba j7+ Self-Emptying Vacuum Cleaning Robot - Certified Refurbished!"
      },
      {
        "level": "h3",
        "text": "iRobot Roomba i4+ EVO (4550) Self-Emptying Robot Vacuum - Certified Refurbished!"
      },
      {
        "level": "h3",
        "text": "Anker Soundcore Motion Boom Plus Portable Bluetooth Speaker Outdoor 80W |Refurb"
      },
      {
        "level": "h3",
        "text": "Microsoft Surface Pro 9 13\" Touch Tablet, Intel i7 16GB/256GB SSD, Graphite"
      },
      {
        "level": "h3",
        "text": "Soundcore Space One Wireless Headphones 40H ANC Playtime 2XStronger Voice Reduct"
      },
      {
        "level": "h3",
        "text": "JBL Endurance Peak 3, Dust and water proof True Wireless active earbuds"
      },
      {
        "level": "h3",
        "text": "eufy Security eufyCam E330 4K Outdoor Security Camera System with 1TB HDD|Refurb"
      },
      {
        "level": "h3",
        "text": "MSI Claw Gaming Handheld 7\" FHD 120Hz Ultra 5-135H 16GB RAM 512GB SSD A1M-052US"
      },
      {
        "level": "h3",
        "text": "HP 15 Laptop 15.6\" HD Pentium Quad-Core N200 8GB 128GB SSD Webcam Win11 Home Red"
      },
      {
        "level": "h3",
        "text": "YI 2pc Home Camera 1080p Wireless IP Security Surveillance System Night Vision"
      },
      {
        "level": "h2",
        "text": "eBay Live"
      },
      {
        "level": "h2",
        "text": "Get 20% off for Labor Day"
      },
      {
        "level": "h3",
        "text": "Electronics"
      },
      {
        "level": "h3",
        "text": "Home and Garden"
      },
      {
        "level": "h3",
        "text": "Fashion"
      },
      {
        "level": "h3",
        "text": "eBay Refurbished"
      },
      {
        "level": "h3",
        "text": "Watches"
      },
      {
        "level": "h3",
        "text": "Handbags"
      },
      {
        "level": "h3",
        "text": "Jewelry"
      },
      {
        "level": "h2",
        "text": "Today's Deals"
      },
      {
        "level": "h3",
        "text": "Samsung Galaxy S21 Ultra 5G 128GB G998U Unlocked - Excellent"
      },
      {
        "level": "h3",
        "text": "Dyson Airwrap Complete Styler | Blue Copper   | Refurbished | First Gen"
      },
      {
        "level": "h3",
        "text": "dreame L20 Ultra Robot Vacuum MopExtend 10.5mm Mop Raising-Certified Refurbished"
      },
      {
        "level": "h3",
        "text": "adidas men Adilette Comfort Slides"
      },
      {
        "level": "h3",
        "text": "Canon EOS R7 Body Mirrorless Camera"
      },
      {
        "level": "h3",
        "text": "NEW Nintendo Switch OLED 64GB Neon Red Blue Joy-Con 2021 Newest+ FAST SHIPPING⭐"
      },
      {
        "level": "h3",
        "text": "12' x 10' Patio Gazebo, Mesh Curtains, Double Vented Steel Roof, Aluminum Brown"
      },
      {
        "level": "h3",
        "text": "Google Pixel Watch 41mm GPS + WiFi + Bluetooth Gold Black Silver Watch - Good"
      },
      {
        "level": "h2",
        "text": "Today's Deals"
      },
      {
        "level": "h3",
        "text": "Samsung Galaxy S21 Ultra 5G 128GB G998U Unlocked - Excellent"
      },
      {
        "level": "h3",
        "text": "Dyson Airwrap Complete Styler | Blue Copper   | Refurbished | First Gen"
      },
      {
        "level": "h3",
        "text": "dreame L20 Ultra Robot Vacuum MopExtend 10.5mm Mop Raising-Certified Refurbished"
      },
      {
        "level": "h3",
        "text": "adidas men Adilette Comfort Slides"
      },
      {
        "level": "h3",
        "text": "Canon EOS R7 Body Mirrorless Camera"
      },
      {
        "level": "h3",
        "text": "NEW Nintendo Switch OLED 64GB Neon Red Blue Joy-Con 2021 Newest+ FAST SHIPPING⭐"
      },
      {
        "level": "h3",
        "text": "12' x 10' Patio Gazebo, Mesh Curtains, Double Vented Steel Roof, Aluminum Brown"
      },
      {
        "level": "h3",
        "text": "Google Pixel Watch 41mm GPS + WiFi + Bluetooth Gold Black Silver Watch - Good"
      },
      {
        "level": "h2",
        "text": "Additional site navigation"
      },
      {
        "level": "h3",
        "text": "Buy"
      },
      {
        "level": "h3",
        "text": "Sell"
      },
      {
        "level": "h3",
        "text": "Tools & apps"
      },
      {
        "level": "h3",
        "text": "eBay companies"
      },
      {
        "level": "h3",
        "text": "Stay connected"
      },
      {
        "level": "h3",
        "text": "About eBay"
      },
      {
        "level": "h3",
        "text": "Help & Contact"
      },
      {
        "level": "h3",
        "text": "Community"
      },
      {
        "level": "h3",
        "text": "eBay Sites"
      }
    ],
    "imgTags": [
      {
        "src": "https://ir.ebaystatic.com/cr/v/c01/EB-19845_NA_123099_RM_Q3_US_CustomerMoments_LaborDayRM_SFC_RW35_SFC_V1_Doodle_150x30_FINAL.jpg",
        "alt": "Get the coupon now",
        "width": "150",
        "height": "30"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Overline Image Left"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "⚡️⚡️Size 10 - Air Jordan 4 Retro White Thunder PREORDER ⚡️⚡️"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "SIZE 12 | REEBOK x ALIENS BB 4000 II MIDS INSPIRED BY ALIENS ROMULUS | FAST SHIP"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Air Jordan 4 White Thunder Men's FQ8138-001 Black/White Size 8.5 - BRAND NEW"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Nigel Sylvester x Air Jordan 4 RM SP  ''Anthracite''  Black Men's  HF4334-004"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Size 10 - Jordan 4 Retro Mid Red Thunder"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "adidas Handball Spezial Preloved Green Gum - IG6192 Men's Shoes"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "🔥 NIKE Air Jordan 4 Retro White Thunder FQ8213-001 GS SIZE 6.5Y / 8W BRAND NEW"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Size 10 - Nike Air Foamposite Pro ben gordon 2016"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "🔥 NIKE Air Jordan 4 Retro White Thunder FQ8213-001  GS SIZE 7Y NEW IN HAND 🔥"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Size 7 - Adidas Yeezy Boost 700 Analog 'EG7596' Men's"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Rolex Day Date President Presidential 36mm 18k Yellow Gold 1803 Circa 1977 $20k"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Rolex Tudor 75190 Prince Date Submariner Mens Amazing Watch Box Papers Tag"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Blancpain Aqualung Fifty Fathoms 1000 Feet Diver Vintage Watch 37mm"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Tudor Pelagos 25500T Black Dial Date 42mm Mens Automatic Divers Wrist Watch"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Rolex Oyster Perpetual DateJust Rhodium Dial 36MM 116234 Watch #LW-13"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Cartier Santos Carree Ref 2961 Two Tone S. Steel / 18K Gold 30mm Automatic Watch"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "HEUER AUTAVIA 2446 CHRONOGRAPH ALL STEEL FABULOUS ORIGINAL DIAL, NICE BEZEL RUNS"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Rolex Datejust Turn-O-Graph 116264 THUNDERBIRD Box Tags & Papers 2007 White 36mm"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "OMEGA Seamaster Aqua Terra 150M 220.10.41.21.10.001 - w/Box, No Papers"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "OMEGA Seamaster Diver 300M Blue Dial Steel Bracelet - 210.30.42.20.03.001"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "iRobot Roomba j7+ Self-Emptying Vacuum Cleaning Robot - Certified Refurbished!"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "iRobot Roomba i4+ EVO (4550) Self-Emptying Robot Vacuum - Certified Refurbished!"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Anker Soundcore Motion Boom Plus Portable Bluetooth Speaker Outdoor 80W |Refurb"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Microsoft Surface Pro 9 13\" Touch Tablet, Intel i7 16GB/256GB SSD, Graphite"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Soundcore Space One Wireless Headphones 40H ANC Playtime 2XStronger Voice Reduct"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "JBL Endurance Peak 3, Dust and water proof True Wireless active earbuds"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "eufy Security eufyCam E330 4K Outdoor Security Camera System with 1TB HDD|Refurb"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "MSI Claw Gaming Handheld 7\" FHD 120Hz Ultra 5-135H 16GB RAM 512GB SSD A1M-052US"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "HP 15 Laptop 15.6\" HD Pentium Quad-Core N200 8GB 128GB SSD Webcam Win11 Home Red"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "YI 2pc Home Camera 1080p Wireless IP Security Surveillance System Night Vision"
      },
      {
        "src": "https://i.ebayimg.com/images/g/VYkAAOSwAfRm0hV9/s-w300.jpg",
        "alt": "Live w/ Hawks Breaks - Topps Series 2 $1 Singles"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTk2WDI2OQ==/z/0vQAAOSw0UdXr3yA/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/rAIAAOSwSAdm06bz/s-w300.jpg",
        "alt": "Funkos with King & Queen!!"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MjkzWDMwMA==/z/igcAAOSwwWhmt6xb/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/CEoAAOSwuw5mynLi/s-w300.jpg",
        "alt": "Live from BreakingBangers! W/Turtle"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTYwMFgxNjAw/z/GPgAAOSwivRhi8ow/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/mbkAAOSwmslm00A6/s-w300.jpg",
        "alt": "Sunday Funday! Join a Break or Grab a Personalz with Game Time Cardz!"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MzAwWDIxNA==/z/-jQAAOSwQ1hlJBp~/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/8~AAAOSwItVm058k/s-w300.jpg",
        "alt": "Funko Super Showdown Sunday"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MzAwWDI2Mg==/z/fTYAAOSwsxxjObLd/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/H1kAAOSwSkZm0I3X/s-w300.jpg",
        "alt": "AnZ Comics Exclusives, Singles, and signed Books Hosted by Saul"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTMzMVgxMTQ3/z/~EEAAOSwph9hsiwV/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/gvEAAOSwt5tm0h9i/s-w300.jpg",
        "alt": "BUCK n GO Psychos Double Header Season 15 Episode 1 Season Premier"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTA5MVgxMDc5/z/QLEAAOSwMs5iuzRE/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/R4oAAOSwDppm0hYk/s-w300.jpg",
        "alt": "[Duplicate] Live w/ Hawks Breaks - Topps Series 2 $1 Singles"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTk2WDI2OQ==/z/0vQAAOSw0UdXr3yA/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/P58AAOSwN0dm0lXa/s-w300.jpg",
        "alt": "Pokemon for the People"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTYwMFgxNjAw/z/-REAAOSwi25iiwK1/$_7.PNG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/PbQAAOSwnbdmzpNr/s-w300.jpg",
        "alt": "BMC Collectibles Breaks 9/1"
      },
      {
        "src": "https://i.ebayimg.com/00/s/NTYyWDc4Mw==/z/RQ0AAOSw9TNhs6VH/$_7.PNG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/RfMAAOSwszBm00sL/s-w300.jpg",
        "alt": "Sunday FUNday TCG Personalz And Singles w/Campus Cardz and Gamez!"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTExNFg4Mjg=/z/MwAAAOSwAyllb9Jf/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/n84AAOSwiYdmzfS7/s-w300.jpg",
        "alt": "Sunday Brunch $1 starts NCBD presale  Marvel, DC, Indie"
      },
      {
        "src": "https://i.ebayimg.com/00/s/NTAwWDUwMA==/z/ydYAAOSw~W1gxJsc/$_7.PNG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/RYwAAOSw-wpmx246/s-w300.jpg",
        "alt": "Vintage & Modern Timepieces Pocket Watches Wristwatches"
      },
      {
        "src": "https://i.ebayimg.com/images/g/1CwAAOSwHzZkSqkK/s-l140.webp"
      },
      {
        "src": "https://i.ebayimg.com/images/g/MH8AAOSwj75mz2EQ/s-w300.jpg",
        "alt": "COINS AND CURRENCY EDITION 258 W/ TIM & DEVIN! FREE SHIPPING 8/30 D"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MzAwWDMwMA==/z/518AAOSwRr1mgC8Y/$_7.PNG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/f3MAAOSwM7Nm0uv2/s-w300.jpg",
        "alt": "2024 Topps Chrome Tennis 1 Case (12 Box) Player Break #2"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTA5NlgxMjQy/z/6WQAAOSwLJ9aIOc8/$_7.JPG"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Samsung Galaxy S21 Ultra 5G 128GB G998U Unlocked - Excellent"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Dyson Airwrap Complete Styler | Blue Copper   | Refurbished | First Gen"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "dreame L20 Ultra Robot Vacuum MopExtend 10.5mm Mop Raising-Certified Refurbished"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "adidas men Adilette Comfort Slides"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Canon EOS R7 Body Mirrorless Camera"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "NEW Nintendo Switch OLED 64GB Neon Red Blue Joy-Con 2021 Newest+ FAST SHIPPING⭐"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "12' x 10' Patio Gazebo, Mesh Curtains, Double Vented Steel Roof, Aluminum Brown"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Google Pixel Watch 41mm GPS + WiFi + Bluetooth Gold Black Silver Watch - Good"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Samsung Galaxy S21 Ultra 5G 128GB G998U Unlocked - Excellent"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Dyson Airwrap Complete Styler | Blue Copper   | Refurbished | First Gen"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "dreame L20 Ultra Robot Vacuum MopExtend 10.5mm Mop Raising-Certified Refurbished"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "adidas men Adilette Comfort Slides"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Canon EOS R7 Body Mirrorless Camera"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "NEW Nintendo Switch OLED 64GB Neon Red Blue Joy-Con 2021 Newest+ FAST SHIPPING⭐"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "12' x 10' Patio Gazebo, Mesh Curtains, Double Vented Steel Roof, Aluminum Brown"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Google Pixel Watch 41mm GPS + WiFi + Bluetooth Gold Black Silver Watch - Good"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      }
    ],
    "responseBody": "",
    "viewport": "width=device-width, initial-scale=1, user-scalable=yes, minimum-scale=1",
    "X-UA-Compatible": "IE=edge",
    "360-site-verification": "5f0e3731bf6d3fc8b2f58b1a585a788f",
    "fb:app_id": "102628213125203",
    "content-language": "en-us",
    "msvalidate.01": "34E98E6F27109BE1A9DCF19658EEEE33",
    "referrer": "unsafe-url",
    "y_key": "acf32e2a69cbc2b0",
    "google-site-verification": "8kHr3jd3Z43q1ovwo0KVgo_NZKIEMjthBxti8m8fYTg",
    "google-adsense-account": "sites-7757056108965234",
    "yandex-verification": "6e11485a66d91eff"
  },
  "code": 200
}
```

---

## Customer Support

Need any assistance? [Get in touch with Customer Support](https://apiverve.com/contact).

---

## Updates
Stay up to date by following [@apiverveHQ](https://twitter.com/apiverveHQ) on Twitter.

---

## Legal

All usage of the APIVerve website, API, and services is subject to the [APIVerve Terms of Service](https://apiverve.com/terms) and all legal documents and agreements.

---

## License
Licensed under the The MIT License (MIT)

Copyright (&copy;) 2024 APIVerve, and Evlar LLC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.