🚓 Los Angeles Crime Data Analysis
📌 Project Overview

Los Angeles is famous for Hollywood, beaches, and year-round sunshine—but like any major city, it also faces significant crime.
This project analyzes real LAPD crime records to uncover key patterns that can help authorities allocate resources more effectively.

The analysis answers three important questions:

Peak Crime Hour – At what time of day do most crimes occur?

Night Crime Hotspot – Which area reports the highest number of late-night crimes?

Victim Age Groups – Which age groups are most frequently targeted?

🗂️ Dataset

File: crimes.csv(not uploaded because of size)

Source: Modified from Los Angeles Open Data

Key Columns:

TIME OCC – Time of occurrence (24-hour format, e.g., 2230 = 10:30 PM)

AREA NAME – One of 21 LAPD divisions (e.g., Hollywood, Central, 77th Street)

Vict Age – Victim’s age

Other details include crime type, weapon used, and victim demographics.

🔑 Key Findings
Question	                                   Answer (Stored in Code)
Hour with the most crimes	peak_crime_hour = 12 (≈ 12:00 PM)
Area with most night crimes (10 PM–3:59 AM)	peak_night_crime_location
Crime counts by victim age group	victim_ages (pandas Series with age brackets as index)
🧮 How It Was Done

Extracted Hour of Crime – Took the first two digits of TIME OCC to get the crime hour.

Night Crime Filter – Selected crimes occurring between 10 PM (22) and 3:59 AM (03) and grouped by AREA NAME.

Age Grouping – Used pd.cut() to divide victim ages into labeled ranges:

0-17, 18-25, 26-34, 35-44, 45-54, 55-64, 65+.

Visualized Trends – Created bar plots to show crime frequency by hour and by age bracket.

📊 Insights

Noon (12 PM) is the single most common hour for crimes in Los Angeles.

[Insert value of peak_night_crime_location] is the hotspot for late-night crimes.

Age group frequencies (example output):

⚙️ Tools Used

Python – Data cleaning & analysis

pandas & NumPy – Data manipulation and grouping

Matplotlib & Seaborn – Visualizations
