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
        "text": "Embrace elegance with 15% off"
      },
      {
        "level": "h2",
        "text": "Trending in Sneakers"
      },
      {
        "level": "h3",
        "text": "Air Jordan 4 Retro Oxidized Green FQ8138-103 IN HANDS SHIPS NOW"
      },
      {
        "level": "h3",
        "text": "Size 12 - Nike Zoom KD 4 2024 Nerf"
      },
      {
        "level": "h3",
        "text": "ASICS GT-2160 Kith Marvel Villains Spider-Man Venom Pack Sealed Box Size 12"
      },
      {
        "level": "h3",
        "text": "Nike Jordan 4 Retro Military Blue 2024 (FV5029-141) Men's Size 7-14"
      },
      {
        "level": "h3",
        "text": "2011 Nike Zoom KD IV 4 Nerf PROMO SAMPLE Size 10.5 DS"
      },
      {
        "level": "h3",
        "text": "Size 10 - On Cloud 5 All Black"
      },
      {
        "level": "h3",
        "text": "Size 11.5 - Nike Zoom KD 4 2024 Nerf FQ8180-400 🔫 Order Confirmed!"
      },
      {
        "level": "h3",
        "text": "Size 10.5 - Jordan 4 Retro OG Mid Bred 2019"
      },
      {
        "level": "h3",
        "text": "Air Jordan 1 Retro high OG (travis Scott mocha)100% authentic size 10.5"
      },
      {
        "level": "h3",
        "text": "ASICS GEL-1130 Kith Marvel Super Villains Magneto Size 6 Confirmed"
      },
      {
        "level": "h2",
        "text": "Trending in Watches"
      },
      {
        "level": "h3",
        "text": "Omega Seamaster Planet Ocean 2200.50.00 45mm Priced to sell"
      },
      {
        "level": "h3",
        "text": "Vintage Rare Rolex Tudor Submariner Ref 76100 Blue Dial 40mm 1984 NO RESERVE"
      },
      {
        "level": "h3",
        "text": "Ladies 18k Cartier Panthère Ref. 1070 Silver Roman Dial 22mm Full Set #W101919-1"
      },
      {
        "level": "h3",
        "text": "Vintage Omega Speedmaster Professional 145.022-74 ST Black Dial 42mm #W108872-1"
      },
      {
        "level": "h3",
        "text": "Rolex OP Datejust Ref.16013 Champagne Dial 36mm w/ Service Box #W109474-1"
      },
      {
        "level": "h3",
        "text": "ROLEX 34mm AIR-KING SILVER BLUE DIAL STAINLESS STEEL AUTOMATIC WATCH 114200"
      },
      {
        "level": "h3",
        "text": "Rolex Oyster Perpetual Date Submariner Ref.16610 Black Dial 40mm #W108582-1"
      },
      {
        "level": "h3",
        "text": "Rolex 41mm Fluted Bezel Wimbledon Dial Jubilee Bracelet 2022"
      },
      {
        "level": "h3",
        "text": "Domino's Pizza Rolex Oyster Perpetual 36 Ref. 126000 Silver Dial 36mm #W907448-1"
      },
      {
        "level": "h3",
        "text": "Rolex Datejust 16233 Gold and Silver Jubilee 36mm *NO RESERVE*"
      },
      {
        "level": "h2",
        "text": "Score these trending kicks"
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
        "text": "Jordan 4 Retro Military Blue 2024"
      },
      {
        "level": "h3",
        "text": "Jordan 4 Bred Reimagined"
      },
      {
        "level": "h3",
        "text": "Jordan 4 Retro Oxidized Green"
      },
      {
        "level": "h3",
        "text": "Jordan 4 Retro Military Black"
      },
      {
        "level": "h3",
        "text": "Jordan 4 Retro Black Cat"
      },
      {
        "level": "h2",
        "text": "Trending in Refurbished"
      },
      {
        "level": "h3",
        "text": "Edifier R1280T Bookshelf Speakers Studio Monitor Speaker - Certified Refurbished"
      },
      {
        "level": "h3",
        "text": "iRobot Roomba i4+ EVO (4550) Self-Emptying Robot Vacuum - Certified Refurbished!"
      },
      {
        "level": "h3",
        "text": "JBL PartyBox Encore, Portable party speaker with 100W powerful sound"
      },
      {
        "level": "h3",
        "text": "JBL Xtreme 2 Portable Bluetooth Speaker"
      },
      {
        "level": "h3",
        "text": "Soundcore Space A40 SE True Wireless Earbuds Adaptive Noise Cancelling Hi-Res"
      },
      {
        "level": "h3",
        "text": "Microsoft Surface Pro 9 13\" Touch Tablet, Intel i7 16GB/256GB SSD, Graphite"
      },
      {
        "level": "h3",
        "text": "2023 HP 17-cn3053cl 17.3\" IPS FHD Laptop Intel Core i5-1335U 12GB 512GB SSD W11"
      },
      {
        "level": "h3",
        "text": "Soundcore Space A40 Wireless Earbuds Auto-Adjustable Active Noise Cancelling"
      },
      {
        "level": "h3",
        "text": "SimpliSafe 13 Piece Wireless Home Security System With Indoor Camera & Doorbell"
      },
      {
        "level": "h3",
        "text": "Lenovo IdeaPad 1 14IGL7 14\" HD Laptop Intel Cel N4020 4GB 128GB 82V6007ECF W11H"
      },
      {
        "level": "h2",
        "text": "eBay Live"
      },
      {
        "level": "h2",
        "text": "Fresh finds for the first day of school"
      },
      {
        "level": "h3",
        "text": "Up to 40% off sneakers"
      },
      {
        "level": "h3",
        "text": "Up to 60% off essentials"
      },
      {
        "level": "h3",
        "text": "Up to 50% off dorm room needs"
      },
      {
        "level": "h3",
        "text": "Up to 70% off laptops"
      },
      {
        "level": "h3",
        "text": "Up to 70% off speakers and more"
      },
      {
        "level": "h3",
        "text": "Smartphones under $500"
      },
      {
        "level": "h3",
        "text": "Up to 50% off instruments"
      },
      {
        "level": "h2",
        "text": "Today's Deals"
      },
      {
        "level": "h3",
        "text": "Crocs Men's Sneakers - Literide 360 Pacer Lace Up Tennis Shoes for Walking"
      },
      {
        "level": "h3",
        "text": "Apple iPhone 11 - 64GB - Fully Unlocked - ALL CARRIERS - VERY GOOD condition"
      },
      {
        "level": "h3",
        "text": "Dyson Cinetic Big Ball Animal Allergy Upright Vacuum | Nickel | Refurbished"
      },
      {
        "level": "h3",
        "text": "Lenovo ThinkPad X1 Carbon Gen 12 Intel Laptop, 14\" IPS  Low Power,  Ultra 5 125U"
      },
      {
        "level": "h3",
        "text": "Samsung Galaxy S21 5G 128GB G991U Unlocked - Good"
      },
      {
        "level": "h3",
        "text": "Legion 5i 16\" WQXGA 165Hz Gaming Laptop i7-14650HX 16GB RAM 512GB SSD RTX 4060"
      },
      {
        "level": "h3",
        "text": "Apple Watch Ultra 2 2nd Generation GPS & Cellular 49mm - Titanium - Excellent"
      },
      {
        "level": "h3",
        "text": "Creality Falcon 2 Laser Engraver 22W CNC DIY Laser Engraving Cutter for Metal"
      },
      {
        "level": "h2",
        "text": "Today's Deals"
      },
      {
        "level": "h3",
        "text": "Crocs Men's Sneakers - Literide 360 Pacer Lace Up Tennis Shoes for Walking"
      },
      {
        "level": "h3",
        "text": "Apple iPhone 11 - 64GB - Fully Unlocked - ALL CARRIERS - VERY GOOD condition"
      },
      {
        "level": "h3",
        "text": "Dyson Cinetic Big Ball Animal Allergy Upright Vacuum | Nickel | Refurbished"
      },
      {
        "level": "h3",
        "text": "Lenovo ThinkPad X1 Carbon Gen 12 Intel Laptop, 14\" IPS  Low Power,  Ultra 5 125U"
      },
      {
        "level": "h3",
        "text": "Samsung Galaxy S21 5G 128GB G991U Unlocked - Good"
      },
      {
        "level": "h3",
        "text": "Legion 5i 16\" WQXGA 165Hz Gaming Laptop i7-14650HX 16GB RAM 512GB SSD RTX 4060"
      },
      {
        "level": "h3",
        "text": "Apple Watch Ultra 2 2nd Generation GPS & Cellular 49mm - Titanium - Excellent"
      },
      {
        "level": "h3",
        "text": "Creality Falcon 2 Laser Engraver 22W CNC DIY Laser Engraving Cutter for Metal"
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
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": ""
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "'A Breitling Superocean Heritage II Chronograph steel auto watch and a Cartier Ballon Bleu De Cartier Automatic 33 mm stainless steel watch against a brown background. '"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Lenovo"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "KitchenAid"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "New Balance"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Lenovo"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "KitchenAid"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "New Balance"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Air Jordan 4 Retro Oxidized Green FQ8138-103 IN HANDS SHIPS NOW"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Size 12 - Nike Zoom KD 4 2024 Nerf"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "ASICS GT-2160 Kith Marvel Villains Spider-Man Venom Pack Sealed Box Size 12"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Nike Jordan 4 Retro Military Blue 2024 (FV5029-141) Men's Size 7-14"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "2011 Nike Zoom KD IV 4 Nerf PROMO SAMPLE Size 10.5 DS"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Size 10 - On Cloud 5 All Black"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Size 11.5 - Nike Zoom KD 4 2024 Nerf FQ8180-400 🔫 Order Confirmed!"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Size 10.5 - Jordan 4 Retro OG Mid Bred 2019"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Air Jordan 1 Retro high OG (travis Scott mocha)100% authentic size 10.5"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "ASICS GEL-1130 Kith Marvel Super Villains Magneto Size 6 Confirmed"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Omega Seamaster Planet Ocean 2200.50.00 45mm Priced to sell"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Vintage Rare Rolex Tudor Submariner Ref 76100 Blue Dial 40mm 1984 NO RESERVE"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Ladies 18k Cartier Panthère Ref. 1070 Silver Roman Dial 22mm Full Set #W101919-1"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Vintage Omega Speedmaster Professional 145.022-74 ST Black Dial 42mm #W108872-1"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Rolex OP Datejust Ref.16013 Champagne Dial 36mm w/ Service Box #W109474-1"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "ROLEX 34mm AIR-KING SILVER BLUE DIAL STAINLESS STEEL AUTOMATIC WATCH 114200"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Rolex Oyster Perpetual Date Submariner Ref.16610 Black Dial 40mm #W108582-1"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Rolex 41mm Fluted Bezel Wimbledon Dial Jubilee Bracelet 2022"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Domino's Pizza Rolex Oyster Perpetual 36 Ref. 126000 Silver Dial 36mm #W907448-1"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Rolex Datejust 16233 Gold and Silver Jubilee 36mm *NO RESERVE*"
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
        "alt": "Edifier R1280T Bookshelf Speakers Studio Monitor Speaker - Certified Refurbished"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "iRobot Roomba i4+ EVO (4550) Self-Emptying Robot Vacuum - Certified Refurbished!"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "JBL PartyBox Encore, Portable party speaker with 100W powerful sound"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "JBL Xtreme 2 Portable Bluetooth Speaker"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Soundcore Space A40 SE True Wireless Earbuds Adaptive Noise Cancelling Hi-Res"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Microsoft Surface Pro 9 13\" Touch Tablet, Intel i7 16GB/256GB SSD, Graphite"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "2023 HP 17-cn3053cl 17.3\" IPS FHD Laptop Intel Core i5-1335U 12GB 512GB SSD W11"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Soundcore Space A40 Wireless Earbuds Auto-Adjustable Active Noise Cancelling"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "SimpliSafe 13 Piece Wireless Home Security System With Indoor Camera & Doorbell"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Lenovo IdeaPad 1 14IGL7 14\" HD Laptop Intel Cel N4020 4GB 128GB 82V6007ECF W11H"
      },
      {
        "src": "https://i.ebayimg.com/images/g/7NAAAOSwvJdmvALX/s-w300.jpg",
        "alt": "Pokémon Packs + Boxes + Slabs w/ Jay & Mike! At Night!"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTIwMFgxMjAw/z/8FgAAOSwx1Rhwkyi/$_7.PNG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/pFgAAOSwGeZmvAw~/s-w300.jpg",
        "alt": "NCBD $5 STARTS WITH TROLL"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTYwMFgxNjAw/z/wQ0AAOSwreZl-Phn/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/dawAAOSwyZpmtX5l/s-w300.jpg",
        "alt": "8-13 Big League, Topps Chrome, UD Extended, Artifacts, Synergy, Artifacts"
      },
      {
        "src": "https://i.ebayimg.com/images/g/1CwAAOSwHzZkSqkK/s-l140.webp"
      },
      {
        "src": "https://i.ebayimg.com/images/g/lBYAAOSwZupmtmP4/s-w300.jpg",
        "alt": "COINS AND CURRENCY EDITION 229 W/ TIM! FREE SHIPPING! 8/13 Q"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MzAwWDMwMA==/z/518AAOSwRr1mgC8Y/$_7.PNG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/dL0AAOSw5t5mu2Dn/s-w300.jpg",
        "alt": "AnZ Comics Exclusives, Singles, and signed Books Hosted by"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTMzMVgxMTQ3/z/~EEAAOSwph9hsiwV/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/cBMAAOSw7b9mu8eS/s-w300.jpg",
        "alt": "Hertel's Coins Buck & Go Auction W/ Moon"
      },
      {
        "src": "https://i.ebayimg.com/00/s/OTY2WDE2MDA=/z/rWAAAOSw~xVba48N/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/gG8AAOSwFHpmuPkx/s-w300.jpg",
        "alt": "Tuesday Breakz w/Game Time Cardz! Grab A Spot In A Break/Mixer!"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MzAwWDIxNA==/z/-jQAAOSwQ1hlJBp~/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/R3EAAOSwmfxmvDOi/s-w300.jpg",
        "alt": "New pops w/ Queen"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MjkzWDMwMA==/z/igcAAOSwwWhmt6xb/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/migAAOSwYbxmu2uS/s-w300.jpg",
        "alt": "Funko Pop! Midweek Madness!"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MzAwWDI2Mg==/z/fTYAAOSwsxxjObLd/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/rioAAOSwYJtmuAI9/s-w300.jpg",
        "alt": "8/10  Spider-Man and More!!!  Cheap starts!  Mult-Lot!!!"
      },
      {
        "src": "https://i.ebayimg.com/images/g/1CwAAOSwHzZkSqkK/s-l140.webp"
      },
      {
        "src": "https://i.ebayimg.com/images/g/13EAAOSw3Uxmu7Xu/s-w300.jpg",
        "alt": "Bulk Lots w/ Mags EL152 PT1"
      },
      {
        "src": "https://i.ebayimg.com/00/s/NzUwWDc1MA==/z/faIAAOSwSf9cvc-S/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/B5AAAOSwKLBmuRZ0/s-w300.jpg",
        "alt": "MUTANT CITY LIVE FROM COMICS ELITE PULLING FROM THE VAULT"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTAwWDEwMA==/z/pB0AAOSwIcZjXWyL/$_7.JPG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/0U0AAOSwCG5moB7v/s-w300.jpg",
        "alt": "Live with Ray Lewis from the National Sports Card Convention!"
      },
      {
        "src": "https://i.ebayimg.com/images/g/1CwAAOSwHzZkSqkK/s-l140.webp"
      },
      {
        "src": "https://i.ebayimg.com/images/g/W~wAAOSwEyVmtmdc/s-w300.jpg",
        "alt": "PACK RIPS WITH NALLELY (ENG/SPAN)-POKEMON-LORCANA-SWU- FREE SHIP! 8/13 W"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MzAwWDMwMA==/z/518AAOSwRr1mgC8Y/$_7.PNG"
      },
      {
        "src": "https://i.ebayimg.com/images/g/bk0AAOSw91Zmtq8r/s-w300.jpg",
        "alt": "TUESDAY NIGHT BASEBALL BREAKS @ TOPP TIER WITH JAMES"
      },
      {
        "src": "https://i.ebayimg.com/00/s/MTA4MFgxMDgw/z/1LgAAOSw1PJmD1Ui/$_7.JPG"
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
        "alt": "Crocs Men's Sneakers - Literide 360 Pacer Lace Up Tennis Shoes for Walking"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Apple iPhone 11 - 64GB - Fully Unlocked - ALL CARRIERS - VERY GOOD condition"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Dyson Cinetic Big Ball Animal Allergy Upright Vacuum | Nickel | Refurbished"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Lenovo ThinkPad X1 Carbon Gen 12 Intel Laptop, 14\" IPS  Low Power,  Ultra 5 125U"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Samsung Galaxy S21 5G 128GB G991U Unlocked - Good"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Legion 5i 16\" WQXGA 165Hz Gaming Laptop i7-14650HX 16GB RAM 512GB SSD RTX 4060"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Apple Watch Ultra 2 2nd Generation GPS & Cellular 49mm - Titanium - Excellent"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Creality Falcon 2 Laser Engraver 22W CNC DIY Laser Engraving Cutter for Metal"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Crocs Men's Sneakers - Literide 360 Pacer Lace Up Tennis Shoes for Walking"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Apple iPhone 11 - 64GB - Fully Unlocked - ALL CARRIERS - VERY GOOD condition"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Dyson Cinetic Big Ball Animal Allergy Upright Vacuum | Nickel | Refurbished"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Lenovo ThinkPad X1 Carbon Gen 12 Intel Laptop, 14\" IPS  Low Power,  Ultra 5 125U"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Samsung Galaxy S21 5G 128GB G991U Unlocked - Good"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Legion 5i 16\" WQXGA 165Hz Gaming Laptop i7-14650HX 16GB RAM 512GB SSD RTX 4060"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Apple Watch Ultra 2 2nd Generation GPS & Cellular 49mm - Titanium - Excellent"
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "Creality Falcon 2 Laser Engraver 22W CNC DIY Laser Engraving Cutter for Metal"
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
        "alt": "An AJ4 'White Thunder' sits against a white background."
      },
      {
        "src": "https://ir.ebaystatic.com/pictures/aw/pics/s_1x2.gif",
        "alt": "A graded Aaron Rodgers 2005 rookie card, a graded Chipper Jones 1991 rookie card, and an autographed Emmitt Smith football sit against a white background."
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