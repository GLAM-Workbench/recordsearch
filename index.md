# RecordSearch

This repository contains Jupyter notebooks to work with data from the National Archives of Australia's RecordSearch database.

[RecordSearch](https://recordsearch.naa.gov.au/) is the online collection database of the National Archives of Australia. Based on the [series system](https://www.naa.gov.au/help-your-research/getting-started/commonwealth-record-series-crs-system), RecordSearch provides rich, contextual information about series, items, agencies, and functions.

Unfortunately RecordSearch doesn't provide access to machine-readable data through an API, so we have to resort to screen scraping. The notebooks here make use of either the [RecordSearch Data Scraper](https://wragge.github.io/recordsearch_data_scraper/) or the older [RecordSearch Tools library](https://github.com/wragge/recordsearch_tools) to handle the scraping. I'm in the process of upgrading all the notebooks to use the newer scraper.

See the [RecordSearch section](https://glam-workbench.net/recordsearch/) of the GLAM Workbench for more details.

## Notebook topics

### Harvesting data

* [**Harvest items from a search in RecordSearch**](harvesting_items_from_a_search.ipynb)
* [**Harvest files with the access status of 'closed'**](harvest_closed_files.ipynb)
* [**Harvest recently digitised files from RecordSearch**](harvest_recently_digitised_files.ipynb)
* [**Harvest details of all series in RecordSearch**](harvest_series_data.ipynb)
* [**Harvesting functions from the RecordSearch interface**](harvesting_functions_from_recordsearch.ipynb)
* [**Harvest agencies associated with *all* functions**](get_all_agencies_by_function.ipynb)

### Analysing data

* [**Exploring harvested series data**](series_harvest_basic_stats.ipynb)
* [**How many of the functions are actually used?**](how_many_functions_are_used.ipynb)
* [**Who's responsible?**](display_agencies_by_function.ipynb)

### Useful tools

* [**Download the contents of a digitised file**](get_images_from_a_digitised_file.ipynb)
* [**Get a list of agencies associated with a function**](get_agencies_associated_with_function.ipynb)
* [**DFAT Cable Finder**](Find_cables.ipynb)


## Cite as

See the GLAM Workbench or [Zenodo](https://doi.org/10.5281/zenodo.3544753) for up-to-date citation details.

----

This repository is part of the [GLAM Workbench](https://glam-workbench.github.io/).  
If you think this project is worthwhile, you might like [to sponsor me on GitHub](https://github.com/sponsors/wragge?o=esb).
