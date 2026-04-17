##  Dataset Description

This project is based on multiple aviation datasets that were integrated to provide a complete view of global flight operations.

The final dataset captures relationships between airlines, airports, aircraft, and routes.

---
## Data Cleaning & Analysis Workflow

This project involves multi-dataset integration followed by cleaning and analysis.

---

###  Initial Exploration

* Loaded all datasets:

  * Airports
  * Airlines
  * Airplanes
  * Routes

* Inspected:

  * Structure of each dataset
  * Column consistency
  * Data types
  * Missing values

---

###  Data Cleaning

####  Handling Missing Values

* Identified missing data across multiple datasets
* Decided on appropriate handling based on column importance

---

####  Removing Duplicates

* Checked and removed duplicate rows in all datasets

---

####  Data Type Fixes

* Ensured:

  * IDs are numeric
  * Text fields are clean and consistent

---

####  Text Cleaning

* Standardized:

  * Airport names
  * Airline names
* Removed inconsistencies and formatting issues

---

###  Data Integration (Core Step)

Performed multiple joins to create a unified dataset:

* Routes + Airlines → to get airline names
* Routes + Airports:

  * Source airport details
  * Destination airport details
* Routes + Airplanes → to get aircraft info

Result:

* A final dataset (**full_data**) containing complete route-level information

---

###  Feature Preparation

* Selected relevant columns for analysis
* Removed unnecessary or redundant fields
* Structured the dataset for easier analysis

---

###  Exploratory Data Analysis (EDA)

####  Traffic Analysis

* Analyzed:

  * Flight frequency per route
  * Most active airlines

---

####  Route Analysis

* Identified:

  * Most common routes
  * Connections between major cities

---

####  Airport Analysis

* Identified busiest airports
* Compared traffic distribution

---

####  Pattern Detection

* Looked for:

  * Repeated routes
  * High-density connections

---

###  Key Observations

* Traffic is concentrated on a limited number of routes
* Some airlines dominate specific regions
* Certain airports act as major hubs

---

###  Final Output

A fully integrated dataset that can be used for:

* Network analysis
* Route optimization
* Predictive modeling


##  Data Sources

The analysis is built on four primary datasets:

1. Airports
2. Airlines
3. Airplanes
4. Routes

Each dataset contributes a different aspect of the aviation ecosystem.

---

##  Detailed Features Description

###  Airports Dataset

Contains information about airport locations and identifiers:

* **Airport ID**: Unique identifier
* **Name**: Airport name
* **City / Country**: Geographic location
* **IATA / ICAO codes**: Standard airport codes
* **Latitude / Longitude**: Geographic coordinates
* **Timezone**: Time offset

This dataset is essential for spatial and geographic analysis.

---

###  Airlines Dataset

Describes airline companies:

* **Airline ID**
* **Name**
* **Country**
* **IATA / ICAO codes**
* **Callsign**

This enables analyzing airline operations and competition.

---

###  Airplanes Dataset

Provides information about aircraft types:

* **Aircraft Name**
* **IATA / ICAO codes**

Used to understand which aircraft are used across routes.

---

###  Routes Dataset (Core Dataset)

Represents flight connections:

* **Airline ID**
* **Source Airport ID**
* **Destination Airport ID**
* **Equipment (aircraft type)**
* **Codeshare indicator**

This is the main dataset used for analysis.

---

##  Data Integration Process

A key strength of this project is combining all datasets into a single unified table:

* Routes merged with Airlines → to include airline names
* Routes merged with Airports:

  * Source airport details
  * Destination airport details
* Routes merged with Airplanes → to include aircraft type

The result is a comprehensive dataset (**full_data**) containing complete flight information.

---

##  What the Final Dataset Represents

After integration, each row represents a **flight route**, including:

* Airline operating the route
* Origin and destination airports
* Aircraft used
* Geographic and operational context

---

##  Data Quality Challenges

Several issues were addressed:

* Missing values across multiple datasets
* Inconsistent text formatting (cleaned and standardized)
* Duplicate entries
* Mismatched or incorrect IDs
* Complexity of multi-step joins

These challenges required careful preprocessing and validation.

---

##  Analytical Value

This dataset enables deep analysis such as:

* Identifying busiest routes and airports
* Understanding airline network structures
* Detecting traffic concentration patterns
* Evaluating route efficiency

It also lays the groundwork for:

* Network analysis
* Optimization models
* Predictive analytics

---

##  Why This Project Stands Out

Unlike simple EDA projects, this work involves:

* Multi-source data integration
* Complex joins across datasets
* Data enrichment and transformation

This makes it closer to **real-world data engineering + analysis workflows**.
