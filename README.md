# NoSQL-Challenge: Eat Safe, Love 

The project focuses on food hygiene ratings across establishments in the United Kingdom. It aims to help food critics and magazines make better-informed decisions on where to focus their next article. 

---

## Overview

The UK Food Standards Agency evaluates restaurants and cafes across the country, providing food hygiene ratings to ensure public safety. This project harnesses the power of **NoSQL databases** to:
- Update and analyze food hygiene data.
- Filter key insights for journalistic purposes.
- Explore trends in food safety across the UK.

---

## Setup Instructions

### Prerequisites

Before diving in, make sure you have the following:
- **MongoDB** installed. [Get it here](https://www.mongodb.com/docs/manual/installation/).
- Python 3.x with the libraries `pymongo`, `pandas`, and `pprint`.
- Jupyter Notebook for running the code.

### Steps to Run

1. **Navigate to the Project Directory:**
   ```bash
   cd NoSQL-Challenge
2. **Import the Dataset into MongoDB:**
  ''' bash
  mongoimport --db uk_food --collection establishments --file "your/path/to/establishments.json" --jsonArray
3. **Run Jupyter Notebook**

## Database Updates

Here's what we did with the `establishments` collection:

1. **Added a New Restaurant:**  
   We introduced **Penang Flavours**, a halal restaurant in Greenwich, to the dataset.

2. **Found and Updated BusinessTypeID:**  
   Queried and updated the `BusinessTypeID` for **Restaurant/Cafe/Canteen**.

3. **Removed Establishments in Dover:**  
   Cleaned out all records linked to the **Dover Local Authority**.

4. **Cleaned Up Data Types:**  
   Converted `latitude`, `longitude`, and `RatingValue` from strings to numbers.

---

## Exploratory Analysis

We tackled these key questions:

1. **Which establishments have a hygiene score of 20?**
   - Identified and analyzed top establishments with excellent hygiene.

2. **Which establishments in London have a `RatingValue ≥ 4`?**
   - Queried high-rated establishments in London.

3. **What are the top 5 establishments closest to Penang Flavours?**
   - Used geocoding to identify top-rated neighbors sorted by hygiene.

4. **Which Local Authorities have the most establishments with a hygiene score of 0?**
   - Aggregated poor hygiene ratings grouped by Local Authority.

Each question showcases the power of **NoSQL queries** and Python for insightful data analysis.
