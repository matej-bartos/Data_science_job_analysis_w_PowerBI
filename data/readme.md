# 📊 Data Folder Background

This folder contains 2024 data on data job postings scraped from Google.


## Data Files

The datasets used in this course are a subset of the full dataset for 2024 and come in a variety of forms:

- `job_postings_flat.csv` - A CSV file that contains the data for the job postings in one single table.
- `job_postings_monthly.xlsx` - An Excel file that contains data broken up by months in each sheet.
- `/monthly_files` - A folder that contains the monthly Excel files for the job postings.
- `/star_schema_files` - A folder that contains the star schema files for the job postings.


## Star Schema

For the `\star_schema_files` folder, I've created a star schema for the data that is organized in the following way:

> **NOTE:** We'll go over how to use this dataset in the course for those new to star schemas.



### Tables
1. `job_postings_fact` - shows job postings (1 job posting per row)
2. `company_dim` - displays information on the company
3. `skills_dim` - list of skills and their type 
4. `skills_job_dim` - matches the skills to each job posting

### Relationships

1. `job_postings_fact` - `company_id` -> `company_dim`
2. `job_postings_fact` - `skill_id` -> `skills_dim`
3. `job_postings_fact` - `skill_id` -> `skills_job_dim`
