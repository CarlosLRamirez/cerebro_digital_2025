---
created: 2024-12-30T20:50:15
modified: '"2024-12-30 20:50", "1tc/G12T+6"'
type: 
aliases: 
tags: 
---



Hice este script con ayuda de ChatGTP para generar un archivo indice con la lista de Notas Diarias ubicadas en un archivo específico


```python
import os
from collections import defaultdict
import calendar

# Define the paths
journal_entries_dir = "/Users/carlos.ramirez/My Notes 2024/Daily Notes"
index_file_path = "/Users/carlos.ramirez/My Notes 2024/Mis Apuntes/My_Journal_Entries.md"

# Get the list of journal entry files
journal_files = [f for f in os.listdir(journal_entries_dir) if f.endswith('.md')]

# Mapping of month numbers to names
month_names = {month: calendar.month_name[month] for month in range(1, 13)}

# Organize files by year and month
entries_by_year_month = defaultdict(lambda: defaultdict(list))
for filename in journal_files:
    parts = filename.split('-', 2)
    # Check if the filename has the expected format
    if len(parts) == 3 and parts[2].endswith('.md'):
        year, month, _ = parts
        entries_by_year_month[year][month.zfill(2)].append(filename)  # Ensure month is two digits
    else:
        print(f"Skipping file with unexpected format: {filename}")

# Open the index file for writing
with open(index_file_path, 'w') as index_file:
    index_file.write("# My Journal Entries\n\n")
    for year in sorted(entries_by_year_month.keys()):
        index_file.write(f"## {year}\n\n")  # Year heading
        for month in sorted(entries_by_year_month[year].keys(), key=int):  # Sort by month number
            month_name = month_names[int(month)]  # Convert month number to name
            index_file.write(f"### {month_name}\n\n")  # Use month name as subheading
            # Sort files within each year-month group by full date
            sorted_files = sorted(entries_by_year_month[year][month], key=lambda x: x.split('-', 2))
            for filename in sorted_files:
                # Convert spaces to %20 for URLs
                formatted_filename = filename.replace(' ', '%20')
                # Write the markdown link to the file
                index_file.write(f"- [{filename}](../Daily%20Notes/{formatted_filename})\n")
            index_file.write("\n")  # Add a newline for spacing

print("Index file created successfully with year and month groupings, ordered by date, with month names.")
```
