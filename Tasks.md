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
DONE KAT - pull stations by state to be filtered by coordinates later
NOPE KAT - try to understand station IDs.

What time range should we focus on?
dec 92 = apr 97

Should we only look at specific months of the year?
mnths with ice coverage

NOPE DONE - Should we include Lake St. Clair?
    it's in the ice coverage but not in the stats.

How to identify the separate lakes in NOAA?
    Use MEMET's boxes to separate lakes

What plots to create?
max ice coverage / water area or shoreline


Who is presenting?



## Planning
1 notebook per data source to gather, clean, and export to a new clean csv
DONE datatypes.ipynb = variables_to_use.csv
stations.ipynb = stations_to_use.csv
lake_stats.ipynb = lake_stats.csv
lake_ice.ipynb = ice_coverage.csv
data.ipynb = data.sql

1 notebook for analysis
## 2-3 plots
1. Surface area vs. Max coverage
2. Monthly % coverage scaled by DX32 (average be weighted)
3. Monthly DT32 scaled by DX32
4. Monthly DT32 scaled by number of days with ice. 
all notes for presentation
presentation.ipynb = charts and anything needed for Presentation

Kat will handling merge conflicts.
Notify Kat in slack channel when you have created a pull request in github.
Please include what new completed piece you are adding to master.

Push your branch to github often.
Remember to:
    #Stay on your branch
    git status
    ## DO NOT git add .
    git add <file>
    git commit -m "message"
    #repeat for all files you KNOW you've edited
    git push
    #Pulling changes from master
    git checkout master
    git pull
    git checkout <branch>
    git merge master
    git commit -m "message"
    git push

# Tasks

### Lake Ice Notebook
DONE SAHAR - Convert Date column to DateTime
    test filtering time ranged on date column
DONE KAT - Make Date Column index?
DONE KAT - Remove basin file from notbeook
DONE KAT - understand date distribution in df
Filter by chosen date range
DONE KAT - Export to csv in clean_data directory

### Lake Stats Notebook
DONE KAT - Remove imperial unit rows
DONE KAT - Remove Totals column
DONE MEMET - Find and add coordinates of boxes around each individual lake
        add in new columns for each corner
        in format (lat,long)
DONE KAT - Export to csv in clean_data directory

### DEPRICATED NOAA Notebook
Get data from NOAA
SAHAR - Convert min and max dates to DateTime
SAHAR - filter min and max dates for stations and variables (like Berien's list) based on max and min dates from lake_ice data
Clean data
    Remove duplicate names from stations_df
    Filter stations by elevation, latitude and longitude per lake based on df_lakes in lake_stats notebook
Export to csv(s) in clean_data directory

helpful api from David: https://geo.fcc.gov/api/census/

### Datatypes Notebook
DONE
    
### Stations Notebook
    filter by coordinates and elevation by Lake
    Define Date Range to filter
    export each lake to CSV
    
### Data 
KAT - pull data from API by state and year
        save in batches of 1000
DONE    saved per lake
DONE KAT - filter to only variables in variables_to_use.csv
filter to only stations in stations_to_use.csv
DONE KAT - filter to only dates in date range
    export to sql
    
### Export to sql?!?
Watch videos, take notes and try to export to sql

#### From Ed:
One covers installing local clients and servers for MySQL and loading a database locally. The two others cover the same thing, but with the cloud. I would recommend going in order.
You need to go through them both. The local install will be necessary when we start class on the 22nd/23rd. The remote is a requirement for the projects. We won’t spend class time on this, so please come to us during office hours before.
local: https://codingbootcamp.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=de334b05-9f7f-4d6c-9b33-ab3c016be034
cloud part I: https://codingbootcamp.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=87d4014b-9941-4de2-9fe1-ab3d013ce69e
cloud part II: https://codingbootcamp.hosted.panopto.com/Panopto/Pages/Viewer.aspx?id=0eb61c79-2ff3-4b10-9056-ab3d01426609
PC instructions: https://docs.google.com/document/d/1sejHRoTaP0c7BEvWJNRsFoXoonsYeikdC4V94MCp2r8/edit?usp=sharing