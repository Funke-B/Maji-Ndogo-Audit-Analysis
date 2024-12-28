# Maji Ndogo Audit Analysis
This project analyzes the Maji Ndogo water project database to ensure data integrity, identify discrepancies, and uncover patterns in errors and their causes. It utilizes SQL, data modeling, and reporting to provide actionable insights into database inconsistencies and employee performance.
![Project Overview](./images/IMG_4133.PNG)

## Project Objectives

- Audit the Database: Evaluate the accuracy and reliability of water source quality scores recorded in the database.
- Analyze Relationships: Correct inconsistencies in the Entity-Relationship Diagram (ERD) to align with actual database structure.
- Investigate Patterns: Identify patterns of errors in water quality scores and explore potential causes, including employee performance.
- Provide Recommendations: Highlight areas for improvement to ensure accountability and transparency.

## Tools and Technologies
- SQL: Used for querying, joining datasets, and analyzing data.
- ERD: Designed and updated to reflect accurate database relationships.

## Key Components
- Entity-Relationship Diagram (ERD):
- Visualized the relationships between key tables: visits, water_quality, auditor_report, and employees.
- Corrected cardinality errors (e.g., ensuring one-to-one relationships where applicable).
  
 Data Integration:
- Imported auditor results into the database using SQL scripts:
  DROP TABLE IF EXISTS `auditor_report`;
CREATE TABLE `auditor_report` (
    `location_id` VARCHAR(32),
    `type_of_water_source` VARCHAR(64),
    `true_water_source_score` INT DEFAULT NULL,
    `statements` VARCHAR(255)

- Joined auditor_report with visits and water_quality tables for comparative analysis.

 Data Analysis:
- Discrepancy Analysis: Compared auditor scores with database scores to identify inconsistencies.
- Error Attribution: Linked errors to specific employees using the visits table:

## Findings

- 94% of records matched auditor scores; 6% showed discrepancies.
- Four employees had significantly higher error rates than average.
- Incriminating statements linked errors to potential misconduct.

## Recommendations

- Employee Training: Improve training to reduce human error in data collection.
- Enhanced Oversight: Implement stricter review processes for high-error employees.
- Data Validation: Automate quality checks to flag inconsistencies in real-time.
- Follow-Up Investigation: Investigate employees linked to misconduct for accountability.

## Key Features

1. **Data Integrity Check**: Compared water quality scores from employees and independent auditors to assess discrepancies.
as well as Identified patterns of errors to investigate potential misconduct.
2. **Employee Performance Analysis:**: Tracked and attributed errors to specific employees using the visits and employees tables
 and Ranked employees by error frequency to identify outliers.
3. **Advanced SQL Queries:**: Complex joins, aggregations, and Common Table Expressions (CTEs) to manage and analyze data efficiently
and Creation of views like Incorrect_records to simplify repeated analysis.

## Database Structure

The project uses the following tables:

- **`visits`**: Logs visits to locations, linking employee assignments with location data and audit results.
- **`auditor_report`**: Contains independent audit findings, including revised water quality scores and anecdotal evidence.
- **`water_quality`**: Contains water quality scores recorded by employees during site visits.
- **`employees`**:Maintains a list of employees and their unique identifiers.

## Access the Full Documentation

Dataset was provided by ALX [project documentation](https://alx.com).
  
