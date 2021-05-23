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

<!-- START RUN INFO -->

## Run these notebooks

There are a number of different ways to use these notebooks. Binder is quickest and easiest, but it doesn't save your data. I've listed the options below from easiest to most complicated (requiring more technical knowledge).

### Using Binder

[![Launch on Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/GLAM-Workbench/recordsearch/master/?urlpath=lab/tree/index.md)

Click on the button above to launch the notebooks in this repository using the [Binder](https://mybinder.org/) service (it might take a little while to load). This is a free service, but note that sessions will close if you stop using the notebooks, and no data will be saved. Make sure you download any changed notebooks or harvested data that you want to save.

See the [Using Binder](https://glam-workbench.net/using-binder/) section of the GLAM Workbench for more details.

### Using Reclaim Cloud

[![Launch on Reclaim Cloud](https://glam-workbench.github.io/images/launch-on-reclaim-cloud.svg)](https://app.my.reclaim.cloud/?manifest=https://raw.githubusercontent.com/GLAM-Workbench/recordsearch/master/reclaim-manifest.jps)

[Reclaim Cloud](https://reclaim.cloud/) is a paid hosting service, aimed particularly at supported digital scholarship in hte humanities. Unlike Binder, the environments you create on Reclaim Cloud will save your data – even if you switch them off! To run this repository on Reclaim Cloud for the first time:

* Create a [Reclaim Cloud](https://reclaim.cloud/) account and log in.
* Click on the button above to start the installation process.
* A dialogue box will ask you to set a password, this is used to limit access to your Jupyter installation.
* Sit back and wait for the installation to complete!
* Once the installation is finished click on the 'Open in Browser' button of your newly created environment (note that you might need to wait a few minutes before everything is ready).

See the [Using Reclaim Cloud](https://glam-workbench.net/using-reclaim-cloud/) section GLAM Workbench [for more details.

### Using Docker

You can use Docker to run a pre-built computing environment on your own computer. It will set up everything you need to run the notebooks in this repository. This is free, but requires more technical knowledge – you'll have to install Docker on your computer, and be able to use the command line.

* Install [Docker Desktop](https://docs.docker.com/get-docker/).
* Create a new directory for this repository and open it from the command line.
* From the command line, run the following command:  
  ```
  docker run -p 8888:8888 --name recordsearch -v "$PWD":/home/jovyan/work glamworkbench/recordsearch repo2docker-entrypoint jupyter lab --ip 0.0.0.0 --NotebookApp.token='' --LabApp.default_url='/lab/tree/index.md'
  ```
* It will take a while to download and configure the Docker image. Once it's ready you'll see a message saying that Jupyter Notebook is running.
* Point your web browser to `http://127.0.0.1:8888`

See the [Using Docker](https://glam-workbench.net/using-docker/) section of the GLAM Workbench for more details.

### Setting up on your own computer

If you know your way around the command line and are comfortable installing software, you might want to set up your own computer to run these notebooks.

Assuming you have recent versions of Python and Git installed, the steps might be something like:

* Create a virtual environment, eg: `python -m venv recordsearch`
* Open the new directory" `cd recordsearch`
* Activate the environment `source bin/activate`
* Clone the repository: `git clone https://github.com/GLAM-Workbench/recordsearch.git notebooks`
* Open the new `notebooks` directory: `cd notebooks`
* Install the necessary Python packages: `pip install -r requirements.txt`
* Run Jupyter: `jupyter lab`

See the GLAM Workbench for more details.

<!-- END RUN INFO -->

## Cite as

See the GLAM Workbench or [Zenodo](https://doi.org/10.5281/zenodo.3544753) for up-to-date citation details.

----

This repository is part of the [GLAM Workbench](https://glam-workbench.github.io/).  
If you think this project is worthwhile, you might like [to sponsor me on GitHub](https://github.com/sponsors/wragge?o=esb).
