# RecordSearch

Current version: [v1.1.0](https://github.com/GLAM-Workbench/recordsearch/releases/tag/v1.1.0)

This repository contains Jupyter notebooks to work with data from the National Archives of Australia's RecordSearch database.

[RecordSearch](https://recordsearch.naa.gov.au/) is the online collection database of the National Archives of Australia. Based on the [series system](https://www.naa.gov.au/help-your-research/getting-started/commonwealth-record-series-crs-system), RecordSearch provides rich, contextual information about series, items, agencies, and functions.

Unfortunately RecordSearch doesn't provide access to machine-readable data through an API, so we have to resort to screen scraping. The notebooks here make use of the [RecordSearch Data Scraper](https://wragge.github.io/recordsearch_data_scraper/).

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

* [**Exploring harvested series data, 2021**](series_harvest_basic_stats.ipynb) – generates some basic statistics from the harvest of series data
* [**Exploring harvested series data, 2022**](series_harvest_basic_stats_2022.ipynb) – generates some basic statistics from the harvest of series data in 2022 and compares the results to the previous year
* [**Summary of records digitised in the previous week**](recently_digitised_update.ipynb) – run this notebook to analyse the most recent dataset of recently digitised files, summarising the results by series
* [**How many of the functions are actually used?**](how_many_functions_are_used.ipynb) – looks at the harvest of functions to see how many are actually in use
* [**Who's responsible?**](display_agencies_by_function.ipynb) – pick a function to which which agencies are have been responsible for it over time

### Useful tools

* [**DIY Redaction Art Collages**](diy_redaction_collage.ipynb) – generates a random sample of ASIO redactions and packs them into one big image
* [**Download the contents of a digitised file**](get_images_from_a_digitised_file.ipynb) – get a digitised files as a folder full of images
* [**Get a list of agencies associated with a function**](get_agencies_associated_with_function.ipynb) - pick a function and create a downloadable list of agencies responsible for it
* [**DFAT Cable Finder**](Find_cables.ipynb) – helps you find numbered cables created by DFAT

## Data downloads

* [Summary data about all series in RecordSearch, May 2021](https://github.com/GLAM-Workbench/recordsearch/blob/master/series_totals_May_2021.csv) (15mb CSV) – contains basic descriptive information about all the series currently registered on RecordSearch (May 2021) as well as the total number of items described, digitised, and in each access category.
* [Summary data about all series in RecordSearch, April 2022](https://github.com/GLAM-Workbench/recordsearch/blob/master/series_totals_April_2022.csv) (15mb CSV) – contains basic descriptive information about all the series currently registered on RecordSearch (May 2021) as well as the total number of items described, digitised, and in each access category.
* [Recently digitised files](https://github.com/GLAM-Workbench/recordsearch/blob/master/data/recently-digitised-20210327) (CSV) – containing details of files digitised between 25 February and 26 March 2021, for an ongoing record of digitised files see [this repository](https://github.com/wragge/naa-recently-digitised) which creates weekly snapsots.

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

See the [Using Reclaim Cloud](https://glam-workbench.net/using-reclaim-cloud/) section of the GLAM Workbench for more details.

### Using the Nectar Research Cloud

The [Nectar Research Cloud](https://ardc.edu.au/services/nectar-research-cloud/) (part of the Australian Research Data Commons) provides cloud computing services to researchers in Australian and New Zealand universities. Any university-affiliated researcher can log on to Nectar and receive [up to 6 months of free cloud computing time](https://tutorials.rc.nectar.org.au/allocation-management/03-account-and-trial). And if you need more, you can [apply for a specific project allocation](https://tutorials.rc.nectar.org.au/allocation-management/04-allocation-and-projects).

The GLAM Workbench is available in the Nectar Cloud as a pre-configured application. This means you can get it up and going without worrying about the technical infrastructure – just fill in a few details and you're away! To create an instance of this repository in the Nectar Cloud:

* Log in to the [Nectar Dashboard](https://dashboard.rc.nectar.org.au/) using your university credentials.
* From the Dashboard choose **Applications -> Browse Local**.
* Enter 'GLAM' in the filter box and hit Enter, you should see the GLAM Workbench application.
* Click on the GLAM Workbench application's  **Quick Deploy** button.
* Step through the various [configuration options](https://glam-workbench.net/using-nectar/#setting-up-your-own-glam-workbench-repository). Some options are only available if you have a dedicated project allocation.
* When asked to select a GLAM Workbench repository, choose 'Reccordsearch' from the dropdown.
* Complete the configuration and deploy your GLAM Workbench instance.
* The url to access your instance will be displayed once it's ready. Click on the url!

See [Using Nectar](https://glam-workbench.net/using-nectar/) for more details.

### Using Docker

You can use Docker to run a pre-built computing environment on your own computer. It will set up everything you need to run the notebooks in this repository. This is free, but requires more technical knowledge – you'll have to install Docker on your computer, and be able to use the command line.

* Install [Docker Desktop](https://docs.docker.com/get-docker/).
* Create a new directory for this repository and open it from the command line.
* From the command line, run the following command:  
  ```
  docker run -p 8888:8888 --name recordsearch -v "$PWD":/home/jovyan/work quay.io/glamworkbench/recordsearch repo2docker-entrypoint jupyter lab --ip 0.0.0.0 --NotebookApp.token='' --LabApp.default_url='/lab/tree/index.ipynb'
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
