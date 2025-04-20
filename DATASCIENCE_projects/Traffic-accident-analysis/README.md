# Prodigy-Infotech-Internship-Task-5

# 🚧 Traffic Accident Analysis – RTA Dataset

This project analyzes road traffic accident data to identify key patterns and contributing factors such as **road conditions**, **weather**, **light conditions**, and **time of day**. It also includes **visualizations of accident hotspots** to support data-driven road safety insights.

---

## 🎯 Objective

- Identify trends and risk factors in road traffic accidents  
- Analyze the influence of environment-related features on accident severity  
- Visualize spatial and temporal accident hotspots  

---

## 📁 Dataset

- **Source:** Provided as `RTA Dataset.csv`  
- **Rows:** ~12,000+  
- **Key Columns:**  
  - `Accident_severity`  
  - `Number_of_casualties`  
  - `Day_of_week`  
  - `Time`  
  - `Light_conditions`  
  - `Weather_conditions`  
  - `Road_surface_conditions`  
  - `Longitude`, `Latitude` *(if available)*  

---

## 🧰 Tools & Libraries

| Library         | Purpose                          |
|-----------------|----------------------------------|
| `pandas`        | Data cleaning & manipulation     |
| `matplotlib`    | Plotting static visualizations   |
| `seaborn`       | Statistical visualization        |
| `plotly`        | Interactive visualizations       |
| `folium`        | Mapping accident hotspots        |

---

## 🧹 Data Cleaning

- Checked and handled missing or inconsistent values  
- Normalized string formats in categorical columns  
- Converted `Time` to proper `datetime` objects  
- Filtered out irrelevant or incomplete entries  

```python
df['Time'] = pd.to_datetime(df['Time'], errors='coerce').dt.hour
df.dropna(subset=['Accident_severity', 'Weather_conditions'], inplace=True)
```

---

## 🔍 Exploratory Data Analysis (EDA)

### 📌 Accident Severity by Road Conditions

```python
sns.countplot(x='Road_surface_conditions', hue='Accident_severity', data=df)
plt.xticks(rotation=45)
```

---

### 🌧️ Weather vs Severity

```python
sns.countplot(x='Weather_conditions', hue='Accident_severity', data=df)
```

---

### 🕒 Time of Day Analysis

```python
sns.histplot(df['Time'], bins=24, kde=True)
plt.title("Accident Frequency by Hour of Day")
```

---

### 📍 Accident Hotspot Mapping *(if latitude & longitude present)*

```python
import folium
from folium.plugins import HeatMap

m = folium.Map(location=[latitude, longitude], zoom_start=10)
HeatMap(data=df[['Latitude', 'Longitude']]).add_to(m)
m.save('accident_hotspots.html')
```

---

## 📈 Key Visuals (Add to `images/` folder)

- `severity_by_road.png`  
- `weather_impact.png`  
- `time_distribution.png`  
- `accident_hotspot_map.png` *(interactive)*  

---

## 🧠 Key Insights

- **Poor road surface and adverse weather** correlate with severe accidents  
- **Most accidents occur during evening peak hours**  
- **Fridays and weekends** show higher accident counts  
- Hotspots cluster around **urban intersections** and **major highways**

---

## 🚀 How to Run

1. Clone the repository:
```bash
git clone https://github.com/yourusername/traffic-accident-analysis.git
cd traffic-accident-analysis
```

2. Install required libraries:
```bash
pip install -r requirements.txt
```

3. Run the Jupyter notebook:
```bash
jupyter notebook Traffic_Accident_Analysis.ipynb
```

---

## 🗂️ Folder Structure

```
Traffic-accident-analysis/
├── RTA Dataset.csv
├── Traffic_Accident_Analysis.ipynb
├── images/
│   └── severity_by_road.png
│   └── weather_impact.png
│   └── time_distribution.png
│   └── accident_hotspot_map.png
└── README.md
```

---

## 🙋 Contact

- 📧 (snehams.1812@gmail.com) 
- 💼 [LinkedIn](https://www.linkedin.com/in/priyanka-mandal-dataenthusiast1812)  

> ⭐ If you find this useful, feel free to star the repo and share your feedback!
