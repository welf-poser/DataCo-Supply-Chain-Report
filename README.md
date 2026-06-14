# DataCo Supply Chain Report

<img width="934" height="592" alt="Screenshot 2026-06-14 095351" src="https://github.com/user-attachments/assets/b2f4a48a-d24b-4643-88c9-b3d0176aca81" />
<img width="920" height="587" alt="Screenshot 2026-06-14 095409" src="https://github.com/user-attachments/assets/1796deb7-e138-4cae-ac57-15a5d4d7e745" />
<img width="934" height="592" alt="Screenshot 2026-06-14 095351" src="https://github.com/user-attachments/assets/c8b2c270-eb49-48f9-8416-15f217cb4bfd" />

A Tableau-based academic visual analytics project using the DataCo Smart Supply Chain dataset.

This project explores how supply-chain data can be transformed into an interactive BI report for monitoring shipment performance, delivery delays, sales, profit and customer-related patterns.

The report was developed in an academic context for an information visualization course and uses concepts from Tamara Munzner's visualization frameworks to structure the design process.

## Project overview

The goal of this project was to design and implement an interactive supply-chain dashboard in Tableau.

The report focuses on three main analytical areas:

* Shipment performance
* Delivery performance
* Sales and customer behavior

The project combines business-oriented dashboard design with a structured visualization methodology. Instead of only building charts, the work documents the reasoning behind the dashboard: domain situation, target users, analytical questions, data and task abstraction, visual encoding decisions and validation.

## Methodological foundation

The dashboard design was guided by concepts from Tamara Munzner's work on information visualization, especially:

* What-Why-How framework
* Nested Model for Visualization Design and Validation
* Visualization Analysis and Design

These frameworks were used to structure the project from the business problem to the final visual representation.

The project follows the idea that effective visualization design should not start with chart selection, but with a clear understanding of:

* what data is available
* why users need to analyze it
* how the data should be visually encoded
* whether the resulting dashboard answers the intended business questions

## Dataset

The project uses the DataCo Smart Supply Chain dataset.

The main dataset contains order-level supply-chain data with information about:

* orders
* shipment and delivery times
* delivery status
* late delivery risk
* products and categories
* customers and customer segments
* markets, regions and countries
* sales, profit and discounts
* shipping modes and payment types

The original dataset contains 180,520 rows and 53 columns. After data preparation, the final Tableau dataset contains 180,516 rows and 41 columns.

## Data preparation

The data preparation was mainly performed with Python before loading the dataset into Tableau.

Main preparation steps:

* inspected missing values
* removed unusable columns with excessive missing values
* removed sensitive customer-related attributes
* removed redundant technical ID columns
* prepared the cleaned dataset for Tableau
* adjusted selected fields inside Tableau
* created calculated fields for analysis

Examples of calculated fields:

* shipment delay
* late delivery indicator
* adjusted late delivery rate
* late delivery prediction accuracy
* aggregated order daytime categories

## Dashboard structure

The Tableau report is organized into three main dashboard pages:

### Shipment

Focuses on shipment performance and compares planned shipment time with actual shipment time.

Example questions:

* How do planned and actual shipment times develop over time?
* Which stores show delayed shipment behavior?
* Are shipment delays related to location, order time or shipping mode?

### Arrival

Focuses on delivery performance and late delivery behavior.

Example questions:

* How often do late deliveries occur?
* How accurate is the late delivery risk prediction?
* Are delivery delays related to destination states, shipment modes or order patterns?

### Sales and Customers

Focuses on sales, profit and customer-related business metrics.

Example questions:

* How do sales and profit develop over time?
* Where are customers located?
* Which products are most frequently ordered?
* Which payment methods are preferred?

## Visualization design

The dashboard uses a deliberately conservative visual design to support quick interpretation by business users.

Main visualization types:

* line charts for time-based trends
* maps for geographic patterns
* bar charts and histograms for distributions and comparisons
* KPI text cards for quick executive-level metrics
* a pie chart for high-level payment method distribution

Color encoding follows a simple semantic pattern:

* red for negative or critical values
* green for positive values
* blue for neutral quantitative distributions
* additional colors for categorical separation where needed

The dashboard design prioritizes readability, orientation and practical business interpretation over experimental visualization techniques.

## Repository contents

| File                                    | Description                                                                                                  |
| --------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| `Supply_Chain_Report.twbx`              | Tableau packaged workbook containing the interactive report                                                  |
| `Dokumentation_Supply_Chain_Report.pdf` | Full academic documentation of the design process, methodology, data preparation and visualization decisions |

## Project status

This is a legacy academic / portfolio project.

It is kept public because it demonstrates early practical experience with:

* Tableau dashboard development
* BI reporting
* information visualization methodology
* supply-chain data analysis
* data preparation for reporting
* structured documentation of design decisions

It is not intended to represent a production-grade BI platform or a modern analytics engineering workflow.

## Potential improvements

If this project were modernized today, the following improvements would be useful:

* add dashboard screenshots directly to the repository
* add an executive summary of the main findings
* document the dataset source and license more clearly
* add a `assets/` folder for visual examples
* add a short explanation of the core KPIs
* add a reproducible data preparation script
* rebuild the project in Power BI for comparison
* model the dataset with SQL or dbt before visualization
* add a more polished case-study structure
* separate business requirements, data model and dashboard documentation more clearly

## Disclaimer

This project was created in an academic context for learning and portfolio purposes.

It is not a production BI solution and should be understood as a visual analytics and dashboard design exercise.
