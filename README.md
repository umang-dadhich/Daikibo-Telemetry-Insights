# Daikibo-Telemetry-Insights-
data analysis and forensic technology  Created a data dashboard using Tableau  Used Excel to classify data and draw business conclusions

![Screenshot (4897)](https://github.com/user-attachments/assets/e8224d4f-a0cd-4836-bee6-e057424d2028)

![Screenshot (4898)](https://github.com/user-attachments/assets/d5581baa-8018-4bea-9f0e-81b3645afd5d)

# Deloitte Data Analysis Task: Daikibo Telemetry Insights

## Objective

Analyze telemetry data from Daikibo's manufacturing equipment using Tableau. Identify machine downtimes by status flags, visualize device-specific downtime, and create an interactive dashboard by factory.

---

## 📁 Dataset

- **File Format**: JSON  
- **Filename**: `daikibo-telemetry-data.json`  
- **Source**: Provided by Deloitte

---

## 🛠️ Tools Used

- **Tableau Desktop** (Trial version acceptable)
- **Data Format**: JSON

---

## ✅ Task Checklist

### 1. Import the Data into Tableau

- Launch Tableau Desktop.
- On the home screen, click `JSON file` and locate `daikibo-telemetry-data.json`.
- Once imported, **check all schema levels** to make all nested fields available.

### 2. Select Schema Levels

- Ensure that all schema levels are selected:
  - `deviceID`
  - `deviceType`
  - `timestamp`
  - `status`
  - `temperature`
  - `location` (with subfields: `area`, `city`, `country`, `factory`, `section`)

### 3. Create a Calculated Field

- Right-click on any Measure in the Data pane.
- Select `Create Calculated Field`.
- Name the field: **Unhealthy**
- Use the following formula:

```tableau
IF [Status] = "unhealthy" THEN 10 ELSE 0 END
