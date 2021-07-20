# corona-data

[![Go to data collection code](https://img.shields.io/badge/corona-data-yellow)](https://github.com/DrakeRubicon/corona-data)
[![Last commit](https://img.shields.io/github/last-commit/DrakeRubicon/corona-data)](https://github.com/DrakeRubicon/corona-data/commits/main)

Raw data. Scraped, API'ed, screenshot'ed or manually added based upon daily/weekly updates of its sources.

Mostly Saxony, but some contain Datasets for whole Germany too.

## Notice:

* Tagesbericht Meißen for 02.12.2020 and 03.12.2020 was not generated on their servers.
* Datawrapper export for DIVI and Chemnitz for Jan 02 2021 failed. Closest Data Point is Jan 03 2021 12:44pm.
* OpenData-Export for Dresden failed on 10.03.2021 – manually added the table Export, has different structure.
* Daily Report LK Erzgebirgskreis on 18.03.2021 is the same as 17.03. because LK could not provide its own data because of RKI-Dashboard outage. Affects case- & death-numbers of 17.03. as well as incidence and quarantine count on 18.03.
* Meißen did not provide an daily report for 28.03., 30.05. and 12.06.2021 on their servers
* Global collection failed on 16.07.2021. Manually collected data & scrapes on 17.07.2021 10:29am. This should have not resulted in data loss because only two LK's currently update their data on weekends. Those who do tend to update after 12:00pm.
