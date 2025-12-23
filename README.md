# MLB_putaway_pitches
This project analyzes MLB pitcher put-away pitches using Statcast pitch-level data, focusing on where and how pitchers generate strikeouts.<br>
It features an efficient, cached data pipeline to create visualizations designed to scale from individual pitchers up to full pitching staffs.

<b>Project Goals</b><br>
* Identify a pitcher's primary put-away pitches
* Create visualization of put-away pitch locations by pitch type
* Compute put-away pitch usage percentages
* Build a fast and reusable pipeline for future analysis
* Be capable of cross team and league-wide analysis

<b> What is a put-away pitch?</b><br>
The final pitch of a plate appearance that results in a strikeout.

<b>Pipeline Philosophy</b><br>
* Separating conerns
    - Data ingestion, storage, transformation, and visualization are heandled independently
* Persistent storage
    - Raw Statcast data saved to a CSV file, avoiding repeated API calls
* Scalability
    - Works for one individual pitcher, an entire pitching staff, multiple teams, and multiple seasons
 
<b>Project Details:</b><br>
* Cached Statcast data pulls into a locally saved CSV
* Pitcher ID look up table to aquire Statcast player ID for any pitcher
* Put-away pitch percentage breakdown

<b>Required Python Libraries</b><br>
* os - manages cached CSV files
* pandas - work with the data including filter/aggregation/percentage calculations
* matpoltlib - create visualizations
* pybaseball - access to Statcast data

If any of these libraries are needed:<br>
  pip install pandas matplotlib pybaseball
