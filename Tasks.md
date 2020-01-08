## Decisions

BERNIE - What variables to use from NOAA?
What stations to use from NOAA?

Should we include Lake St. Clair?
    it's in the ice coverage but not in the stats.
    EXCLUDE
How to identify the separate lakes in NOAA?

What plots to create?

Who is presenting?

## Planning
1 notebook per data source to gather, clean, and export to a new clean csv

1 notebook for analysis
2-3 plots
all notes for presentation

Kat will handling merge conflicts.
Notify Kat in slack channel when you have created a pull request in github.
Please include what new completed piece you are adding to master.

Push your branch to github often.

# Tasks

### Lake Ice Notebook
SAHAR - Convert Date column to DateTime
    test filtering time ranged on date column
Make Date Column index?
Remove basin file from notbeook
Export to csv in clean_data directory

### Lake Stats Notebook
KAT - Remove imperial unit rows
KAT - Remove Totals column
MEMET - Find and add coordinates of boxes around each individual lake
        add in new columns for each corner
Export to csv in clean_data directory

### NOAA Notebook
Get data from NOAA
SAHAR - Convert min and max dates to DateTime
Clean data
    Remove duplicate names from stations_df
    Filter stations by elevation, latitude and longitude per lake based on df_lakes in lake_stats notebook
Export to csv(s) in clean_data directory

helpful api from David: https://geo.fcc.gov/api/census/

