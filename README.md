# databrary-analytics
Code to produce and plot analytics about Databrary

*- `visits-downloads.Rmd` produces plots and tables from a March 2018 analysis of unique visits and downloads of the site.*   
    *- `visit-downloads.md` shows the output.*   
*- `databrary-user-growth.Rmd` produces a plot of the growth in authorized users and institutions.*   
*- `databrary_monthly.Rmd` produces a combined report on Databrary. An [HTML](https://gilmore-lab.github.io/databrary-analytics/databrary_monthly.html) version is also available.*   
- `databrary_weekly_rpt.Rmd` produces a combined report about Databrary. It is run approximately weekly. An [HTML](https://gilmore-lab.github.io/databrary-analytics/weekly/databrary_weekly_report.html) version is available at the link.  

## Weekly report

- To update the report:  
    - `source('weekly/R/helpers.R')`  
    - `update_weekly_report(db_account = "<YOUREMAIL@YOURDOMAIN>")`  
        - where `YOUREMAIL@YOURDOMAIN` is replaced by your Databrary account. 

- To run the report without updating:
    - `source('weekly/R/helpers.R')`  
    - `render_weekly_report(db_account = "<YOUREMAIL@YOURDOMAIN>")`  
        - where `YOUREMAIL@YOURDOMAIN` is replaced by your Databrary account. 

- View the [current report](https://gilmore-lab.github.io/databrary-analytics/weekly/databrary_weekly_report.html).  

# Citation Data

- These numbers are from the Databrary Actitity site https://nyu.databrary.org/api/activity  

- "Databrary" and "Datavyu" (with quotes) are used to reduce bad hits in [Google Scholar](https://scholar.google.com)      
    - choose the 'anytime' option for Citations Monthly  
    - choose 'Since 2019' option for Citations Yearly  
    - the boxes for *Include Patents* and *Include Citations* remain unchecked  

# Shared volumes and owners report

- [Report](https://gilmore-lab.github.io/databrary-analytics/shared-volumes-sessions/shared-volumes-sessions.html) about full shared volumes and volume overviews only with session statistics.* 
    - To run this report run  
        -`rmarkdown::render("shared-volumes-sessions/shared-volumes-sessions.Rmd", params = list(db_login = "<YOUREMAIL@YOURDOMAIN>"))`
        - replacing `<YOUREMAIL@YOURDOMAIN>` with your actual Databrary login (email).
        
# Tags and keywords report

- [Report](https://gilmore-lab.github.io/databrary-analytics/tags-keywords/tags-keywords-report.html) on the tags and keywords linked to Databrary volumes.
    - To run this report, run `source("tags-keywords/R/helpers.R")` from the R console.
    - Then run `render_tags_keywords_report("<YOUREMAIL@YOURDOMAIN>")`, replacing `<YOUREMAIL@YOURDOMAIN>` with your actual Databrary login (email).

# Institutions and investigators report

- [Report](https://gilmore-lab.github.io/databrary-analytics/institutions-investigators/institutions-investigators.html) on number of investigators at each authorizing institution.
    - To run this report, run `source("institutions-investigators/R/helpers.R")` from the R console.
    - Then run `render_institutions_investigators_report("<YOUREMAIL@YOURDOMAIN>"), replacing `<YOUREMAIL@YOURDOMAIN>` with your actual Databrary login (email).

# Participant demographics report

- [Report](https://gilmore-lab.github.io/databrary-analytics/participant-demographics/participant-demog-report.html) on the site-wide reported participant demographics.
    - To run this report, run `source("participant-demographics/R/helpers.R")` from the R console.
    - Then run `rmarkdown::render("participant-demographics/participant-demog-report.Rmd", params = list(db_login="<YOUREMAIL@YOURDOMAIN>"))`, replacing `<YOUREMAIL@YOURDOMAIN>` with your actual Databrary login (email).