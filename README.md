# group_project_2

# Import dependencies

This project requires the following dependencies:

- pandas
- numpy

### Extract the crowdfunding.xlsx Data

To extract the data from the `crowdfunding.xlsx` file, perform the following steps:

1. Read the data into a Pandas DataFrame using the `read_excel()` function from the pandas library.
2. Display the first few rows of the DataFrame using the `head()` method.
3. Get a summary of the DataFrame using the `info()` method.

### Create the Category and Subcategory DataFrames

To create the Category and Subcategory DataFrames, follow these steps:

1. Create a Category DataFrame with two columns: "category_id" and "category". The "category_id" column should contain sequential numbers from 1 to the length of the number of unique categories, and the "category" column should contain the unique categories.
2. Export the Category DataFrame as a CSV file named `category.csv`.
3. Create a Subcategory DataFrame with two columns: "subcategory_id" and "subcategory". The "subcategory_id" column should contain sequential numbers from 1 to the length of the number of unique subcategories, and the "subcategory" column should contain the unique subcategories.
4. Export the Subcategory DataFrame as a CSV file named `subcategory.csv`.

### Campaign DataFrame

To create the Campaign DataFrame, perform the following steps:

1. Create a copy of the `crowdfunding_info_df` DataFrame named `campaign_df`.
2. Rename the columns "blurb", "launched_at", and "deadline" to "description", "launch_date", and "end_date" respectively, using the `rename()` method.
3. Convert the "goal" and "pledged" columns to float data type using the `astype()` method.
4. Format the "launch_date" and "end_date" columns to datetime format using the `to_datetime()` method.
5. Rename the "subcategory" column to "sub-category" in the Subcategory DataFrame.
6. Merge the `campaign_df` with the Category and Subcategory DataFrames based on the "category" and "sub-category" columns.
7. Drop unwanted columns using the `drop()` method.
8. Export the cleaned Campaign DataFrame as a CSV file named `campaign.csv`.

### Extract the contacts.xlsx Data

To extract the data from the `contacts.xlsx` file, perform the following steps:

1. Read the data into a Pandas DataFrame using the `read_excel()` function from the pandas library. Use the `header=3` parameter to skip the first three rows.
2. Display the first few rows of the DataFrame using the `head()` method.

### Create the Contacts DataFrame

To create the Contacts DataFrame, follow these steps:

1. Create a Contacts DataFrame with four columns: "contact_id", "first_name", "last_name", and "email". Use the values from the "contact_info" column of the `contact_info_df` DataFrame.
2. Split the "name" column into "first_name" and "last_name" columns using the `str.split()` method.
3. Drop the "name" column using the `drop()` method.
4. Reorder the columns as needed.
5. Export the Contacts DataFrame as a CSV file named `contacts.csv`.