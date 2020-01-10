## Decisions

BERNIE - What variables to use from NOAA?
    WESD - water equivalent of snow on the ground
    WT09 - blowing or drifting snow
    WESF - water equivalent of snowfall
    SNWD - snow depth
    NTP  - storm total precipitation
    DPR  - instantaneous precipitation rate
    WT04 - ice pellets, sleet, snow pellets, or small hail"
    WT01 - fog, ice fog, or freezing fog (may include hea..
    WT10 - tornado, waterspout, or funnel cloud"
    THIC - thickness of ice on water
    PRCP - precipitation 
    
    PTA  - storm total accumulation(storm total precipita...
    
    Define/understand variables. How should we use/compare them?
    

What stations to use from NOAA?
MEMET - coordinates (as listed below)
KAT - pull stations by state to be filtered by coordinates later
KAT - try to understand station IDs.

What time range should we focus on?

DONE - Should we include Lake St. Clair?
    it's in the ice coverage but not in the stats.
    EXCLUDE

How to identify the separate lakes in NOAA?
    Use MEMET's boxes to separate lakes

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
DONE SAHAR - Convert Date column to DateTime
    test filtering time ranged on date column
DONE KAT - Make Date Column index?
DONE KAT - Remove basin file from notbeook
KAT - understand date distribution in df
KAT - Export to csv in clean_data directory

### Lake Stats Notebook
DONE KAT - Remove imperial unit rows
DONE KAT - Remove Totals column
MEMET - Find and add coordinates of boxes around each individual lake
        add in new columns for each corner
DONE KAT - Export to csv in clean_data directory

### NOAA Notebook
Get data from NOAA
SAHAR - Convert min and max dates to DateTime
SAHAR - filter min and max dates for stations and variables (like Berien's list) based on max and min dates from lake_ice data
Clean data
    Remove duplicate names from stations_df
    Filter stations by elevation, latitude and longitude per lake based on df_lakes in lake_stats notebook
Export to csv(s) in clean_data directory

helpful api from David: https://geo.fcc.gov/api/census/


Export to sql?!?