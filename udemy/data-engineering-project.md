---
description: Course by Matthew Schembri, including SQL, Python, Airflow, Docker, CI/CD
---

# Data Engineering Project

## Project Overview

**Step 1: Data Extraction**

* Getting the data we going to use through a Youtube API
* Use a python as main language through a script to extract the data

**Step 2: Data Loading & Transformation**

* Loading implies saving the data to a storage system, usually called a data warehouse, data lake or data lake house. In this project, a data warehouse, that is Postgres
* Transformation meaning we will apply changes to the data to make it more readable or extract the portion of information needed. We will use python again to apply the transformations

> ETL, was traditionally this process, the data would be tranformed and then loaded to the warehouse, but in the pas years there's been a change to ELT, driven by advances in tech since modern data storage solutions can handle large volumes of raw data efficiently

**Step 3: Data Quality Testing**

* The data quality tests are essential to ensure that the data given to the users, f.e. data analysts and scientists, is accurate and reliable, f. e. duplicates or incorrect formats
* We will use a tool called SODA

**Step 4: Functional & End-to-end Testing**

* Testing is a best practice from software development and will set you apart from other data engineers.
* We will do unit test, integration test and end-to-end tests
* We will use two frameworks, Pytest an Unit for unit and integration test, and Airflow's testing features for the end-to-end test

**Step 5: CI/CD Continuous Integration and Continuous Deployment**

* We will use Docker and automated testing
* It helps keep the data pipelines running smoothly when you apply changes to the code
* For this we will use, GitHub actions

## Project's Code
