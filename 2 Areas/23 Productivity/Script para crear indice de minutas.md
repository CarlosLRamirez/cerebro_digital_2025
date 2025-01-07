---
created: 2024-12-30T20:50:12
modified: '"2024-12-30 20:50", "1tc/G12T+6"'
type: 
aliases: 
tags: 
---



```python
import os
from collections import defaultdict
import re

# Define the paths
minutes_dir = "/Users/carlos.ramirez/My Notes 2024/Minutas"
index_file_path = "/Users/carlos.ramirez/My Notes 2024/Escala24x7/Indice de Minutas.md"

# Regular expression to extract date and time from filenames
filename_regex = re.compile(r"Minuta (\d{4}-\d{2}-\d{2}) (\d{4}) - (.*)\.md$")

# Organize files by year, month, and date
minutes_by_date = defaultdict(list)

for filename in os.listdir(minutes_dir):
    match = filename_regex.match(filename)
    if match:
        date, time, _ = match.groups()
        year, month, _ = date.split('-')
        minutes_by_date[(year, month)].append((date, time, filename))
    else:
        print(f"Skipping file with unexpected format: {filename}")

# Open the index file for writing
with open(index_file_path, 'w') as index_file:
    index_file.write("# Meeting Minutes Index\n\n")
    for year_month, entries in sorted(minutes_by_date.items()):
        year, month = year_month
        index_file.write(f"## {year}-{month}\n\n")  # Year-Month heading
        for date, time, filename in sorted(entries):
            # Convert spaces to %20 for URLs
            formatted_filename = filename.replace(' ', '%20')
            # Write the markdown link to the file
            index_file.write(f"- [{filename}](../Minutas/{formatted_filename})\n")
        index_file.write("\n")  # Add a newline for spacing

print("Meeting minutes index file created successfully.")



```
