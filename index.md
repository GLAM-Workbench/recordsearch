# RecordSearch

This repository contains Jupyter notebooks to work with data from the National Archives of Australia's RecordSearch database.

[RecordSearch](https://recordsearch.naa.gov.au/) is the online collection database of the National Archives of Australia. Based on the [series system](https://www.naa.gov.au/help-your-research/getting-started/commonwealth-record-series-crs-system), RecordSearch provides rich, contextual information about series, items, agencies, and functions.

Unfortunately RecordSearch doesn't provide access to machine-readable data through an API, so we have to resort to screen scraping. The notebooks here make use of either the [RecordSearch Data Scraper](https://wragge.github.io/recordsearch_data_scraper/) or the older [RecordSearch Tools library](https://github.com/wragge/recordsearch_tools) to handle the scraping. I'm in the process of upgrading all the notebooks to use the newer scraper.

See the [RecordSearch section](https://glam-workbench.net/recordsearch/) of the GLAM Workbench for more details.

## Notebook topics

### Harvesting data

* [**Harvest items from a search in RecordSearch**](harvesting_items_from_a_search.ipynb) – save the results of an item search in RecordSearch as a downloadable dataset, you can also save images and PDFs from digitised files
* [**Harvest files with the access status of 'closed'**](harvest_closed_files.ipynb) – find out what we're not allowed to see by harvesting details of 'closed' files
* [**Harvest recently digitised files from RecordSearch**](harvest_recently_digitised_files.ipynb) – save details of files digitised in the past month
* [**Harvest details of all series in RecordSearch**](harvest_series_data.ipynb) – get details of all series registered in RecordSearch, also generates a summary dataset with the total number of items digitised, described and in each access category
* [**Harvesting functions from the RecordSearch interface**](harvesting_functions_from_recordsearch.ipynb) – extract information from the RecordSearch interface about the hierarchy of functions it uses to describe the work of government agencies
* [**Harvest agencies associated with *all* functions**](get_all_agencies_by_function.ipynb) – loops through the list of functions saving details of the agencies associated with each

### Analysing data

* [**Exploring harvested series data**](series_harvest_basic_stats.ipynb) – generates some basic statistics from the harvest of series data
* [**How many of the functions are actually used?**](how_many_functions_are_used.ipynb) – looks at the harvest of functions to see how many are actually in use
* [**Who's responsible?**](display_agencies_by_function.ipynb) – pick a function to which which agencies are have been responsible for it over time

### Useful tools

* [**DIY Redaction Art Collages**](diy_redaction_collage.ipynb) – generates a random sample of ASIO redactions and packs them into one big image
* [**Download the contents of a digitised file**](get_images_from_a_digitised_file.ipynb) – get a digitised files as a folder full of images
* [**Get a list of agencies associated with a function**](get_agencies_associated_with_function.ipynb) - pick a function and create a downloadable list of agencies responsible for it
* [**DFAT Cable Finder**](Find_cables.ipynb) – helps you find numbered cables created by DFAT

## Data downloads

* [Summary data about all series in RecordSearch](https://github.com/GLAM-Workbench/recordsearch/blob/master/series_totals_May_2021.csv) (15mb CSV) – contains basic descriptive information about all the series currently registered on RecordSearch (May 2021) as well as the total number of items described, digitised, and in each access category.
* [Recently digitised files](https://github.com/GLAM-Workbench/recordsearch/blob/master/data/recently-digitised-20210327) (CSV) – containing details of files digitised between 25 February and 26 March 2021, for an ongoing record of digitised files see [this repository](https://github.com/wragge/naa-recently-digitised) which creates weekly snapsots.


## Cite as

See the GLAM Workbench or [Zenodo](https://doi.org/10.5281/zenodo.3544753) for up-to-date citation details.

----

This repository is part of the [GLAM Workbench](https://glam-workbench.github.io/).  
If you think this project is worthwhile, you might like [to sponsor me on GitHub](https://github.com/sponsors/wragge?o=esb).
