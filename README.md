# NoSQL Challenge - UCB Bootcamp Challenge #12

The goal of this challenge is to evaluate the ratings data to assist journalists and food critics of the food magazine, Eat Safe, Love, in deciding where to focus future articles.

## Part 1: Database and Jupyter Notebook Setup

The `NoSQL_setup_starter.ipynb` notebook was used for initial setup.

Data from the `establishments.json` file was imported via terminal commands into a MongoDB database named `uk_food` with the collection named `establishments`.

### Verification Steps
To confirm the database and data were correctly set up, the following tasks were completed:
- Listing all databases in MongoDB to confirm `uk_food` is listed.
- Listing the collections in `uk_food` to ensure `establishments` is present.
- Finding and displaying one document from the `establishments` collection using `find_one` and `pprint`.
- Assigning the `establishments` collection to a variable for easier access and manipulation.

## Part 2: Update the Database

Modifications made to the `establishments` collection include:
- Addition of a new halal restaurant named 'Penang Flavors' in Greenwich.
- Retrieval of the `BusinessTypeID` for "Restaurant/Cafe/Canteen" and returning only the `BusinessTypeID` and `BusinessType` fields.
- Updating the newly added restaurant with the `BusinessTypeID` of '1'.
- Deletion of all documents where the Local Authority is named Dover.
- Conversion of `latitude`, `longitude`, and `RatingValue` from strings to numerical values for accurate querying.

## Part 3: Exploratory Analysis

The `NoSQL_analysis_starter.ipynb` notebook facilitated the exploratory analysis with specific queries tailored to the magazine's needs:

### Key Questions and Operations
- Converted non-numeric `RatingValue` fields to nulls during database setup before converting these ratings to integers.
- Displayed the count of documents, the first document, and converted query results to a Pandas DataFrame for the following questions:
  - Which establishments have a hygiene score of 20?
  - Which establishments in London have a `RatingValue` of at least 4?
  - Identified the top 5 establishments with a `RatingValue` of 5, sorted by the lowest hygiene score and proximity to the newly added "Penang Flavours".

- Employed the aggregation framework to determine the number of establishments in each Local Authority area with a hygiene score of 0, sorted the results from highest to lowest, and printed the top ten Local Authority areas.







