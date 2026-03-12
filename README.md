# Delhivery Logistics Operations Analysis

## Project Overview

This project analyzes logistics trip data from Delhivery to understand delivery efficiency, operational patterns, and potential bottlenecks in the logistics network.

The dataset contains trip-level and segment-level information representing the movement of shipments between warehouses and delivery points. Each trip can consist of multiple segments connecting different logistics hubs.

The goal of this analysis is to explore operational performance, identify patterns in delivery times, and uncover insights that could help improve logistics efficiency.

---

## Dataset Description

The dataset includes logistics trip details from **12 September 2018 to 8 October 2018**.

Key characteristics of the dataset:

* Total trips conducted: **14,787**
* Trips are divided into **multiple segments**
* Each segment represents movement between two logistics nodes
* Segments can represent:

  * Warehouse to warehouse movement
    ️- Warehouse to delivery center movement
* Most segment delivery times are **below 700 minutes**, although some extreme values exist due to operational or traffic constraints.

---

## Business Objectives

The analysis focuses on answering the following operational questions:

* What are the key patterns in logistics trip durations?
* Which source hubs handle the highest logistics traffic?
* Are there any extreme delays or anomalies in delivery time?
* How is delivery time distributed across different routes?
* What operational insights can be derived from trip segmentation?

---

## Tools and Technologies

The analysis was conducted using the following tools:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Project Workflow

### 1. Data Cleaning

* Checked for missing values
* Standardized time related variables
* Verified segment consistency within trips
* Identified potential outliers in delivery time

### 2. Exploratory Data Analysis (EDA)

* Distribution of delivery time
* Frequency analysis of logistics hubs
* Segment-level operational analysis
* Trip duration patterns

### 3. Visualization

Visualizations were created to better understand:

* Delivery time distribution
* Most active logistics hubs
* Route traffic concentration
* Outliers and extreme delivery times

---

## Insights

* The dataset contains logistics trip details from **12 September 2018 to 8 October 2018**, during which **14,787 trips** were conducted.

* Trips are composed of multiple **segments**, which are intermediary movements that combine to form a complete trip. These segments typically represent transportation between warehouses or from warehouses to delivery points.

* Most segment delivery times are **below 700 minutes**. However, due to traffic congestion and other operational factors, delivery times can extend up to **4000 minutes** in some cases.

* The majority of delivery distances are **less than 300 kilometers**, although a small number of trips exceed **2000 kilometers**.

* **Inter-state Full Truck Load (FTL)** segments generally take longer to complete due to longer travel distances and the transportation of bulk orders.

* The **Open Source Routing Machine (OSRM)** estimates show high variation when compared with actual delivery times and distances, indicating a strong dependency on road conditions and traffic patterns.

* Hypothesis testing indicates that the **OSRM estimates for delivery time and distance are not sufficiently accurate** when compared with actual operational data.

* Drivers tend to prefer traveling during the **night and early morning hours** to avoid heavy traffic, congestion, and peak business hours.

* The **average handling time for FTL shipments** is higher than for carting shipments because FTL orders typically involve bulk transportation.

* Most **inter-state deliveries are FTL shipments**, while **intra-state deliveries include both FTL and carting**, resulting in higher variability in delivery times.

* Hypothesis testing shows that the **average speed of cart deliveries differs between inter-state and intra-state routes**, although the practical difference is relatively small (approximately **1 km/h**).

* Vehicle speeds vary by time of day. For cart deliveries, vehicles travel **faster during night and late evening hours**.

  * FTL vehicle speed averages **around 35 km/h**, but decreases to **approximately 28 km/h during daytime**.

* The most active logistics hubs in the dataset include:

  * **Gurgaon–Bilaspur**
  * **Bangalore–Nelamangala**
  * **Bhiwandi–Mankoli**

* The **busiest delivery route** identified in the dataset is **Gonda Kotwali to Tulsipur Central**.

---

## Recommendations

* The performance of the **Open Source Routing Machine (OSRM)** shows significant deviation from actual operational data. The business should consider improving routing models or incorporating additional parameters specific to **Indian road and traffic conditions** to produce more accurate delivery time and distance estimates.

* Although the **average speed for inter-state and intra-state shipments is similar**, inter-state deliveries have the potential to be faster since they often involve highway routes.

* High-traffic logistics hubs such as **Gurgaon–Bilaspur, Bangalore–Nelamangala, and Bhiwandi–Mankoli** could benefit from additional **manpower, improved infrastructure, or technological support** to manage high operational volumes.

* Deploying **better or more efficient vehicles for carting shipments** could help optimize delivery times and improve operational efficiency.

* Since logistics operations show **strong dependency on road transportation**, adopting **electric vehicles (EVs)** could help reduce fuel costs and improve long-term operational sustainability.
