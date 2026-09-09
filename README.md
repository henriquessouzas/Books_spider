# Books Spider

A web crawler built with [Scrapy](https://scrapy.org/) that extracts book data from [books.toscrape.com](http://books.toscrape.com/), applying filters by price and rating, and exporting the results to a JSON file.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Output](#output)
- [Project Structure](#project-structure)

---

## Overview

Books Spider crawls all pages of the books.toscrape.com catalogue, collects structured book data, and filters results based on price and star rating criteria. The final dataset is persisted locally as a JSON file.

---

## Features

- Full pagination support — crawls all available pages automatically
- Price filter — includes only books priced at or below £50.00
- Rating filter — includes only books rated Four or Five stars
- JSON export — results are saved with UTF-8 encoding and pretty-printed formatting

---

## Requirements

- Python 3.x
- Scrapy

---

## Installation

Clone the repository and install the required dependency:

```bash
git clone https://github.com/your-username/Books_spider.git
cd Books_spider
pip install scrapy
```

---

## Usage

Run the spider directly with Python:

```bash
python Books.py
```

The crawler will traverse all pages and save the filtered results to `books.json` upon completion.

---

## Output

The output file `books.json` contains an array of objects with the following fields:

| Field | Type | Description |
|---|---|---|
| `title` | string | Book title |
| `price` | float | Price in British pounds |
| `stars` | string | Star rating (`One` to `Five`) |
| `availability` | string | Stock availability status |

Example output:

```json
[
    {
        "title": "Sapiens: A Brief History of Humankind",
        "price": 47.99,
        "stars": "Five",
        "availability": "In stock"
    }
]
```

---

## Project Structure

```
Books_spider/
├── Books.py        # Spider implementation
├── books.json      # Generated output after execution
└── README.md       # Project documentation
```
