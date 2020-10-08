# A1: Data Curation 
The goal of this project is to collect and analyze the data about English Wikipedia page traffic from January 1 2008 to September 30 2020.

## License & Data Use
This project is available under the [MIT License](https://github.com/mshhh/data-512/blob/main/data-512-a1/LICENSE)

Wikimedia Foundation REST API [terms of use](https://www.mediawiki.org/wiki/Wikimedia_REST_API#Terms_and_conditions)

## API Documentation 
I used two different Wikimedia REST API endpoints for gathering the data:

1. The Legacy Pagecounts API: [documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts), [endpoints](https://wikimedia.org/api/rest_v1/#/Pagecounts_data_(legacy)/get_metrics_legacy_pagecounts_aggregate_project_access_site_granularity_start_end)

2. The Pageviews API: [documentation](https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews), [endpoints](https://wikimedia.org/api/rest_v1/#/Pageviews_data/get_metrics_pageviews_aggregate_project_access_agent_granularity_start_end)

## Data File Fields
This directory contains 5 JSON files named as *apiname_accesstype_firstmonth-lastmonth.json*, 1 CSV final data file, 1 Jupyter notebook displaying the whole process, 1 image of data visualization, 1 README file, and 1 LICENSE file. The final data file in CSV follows the format and description as following. 

| Column       | Value         |  Description        | 
| ------------- |-------------|-------------|
| year      | YYYY | the year of data point|
| month      | MM      | the month of the data point|
| pagecount_all_views | num_views      |the number of all page views from the Legacy Pagecounts API|
| pagecount_desktop_views | num_views      |the number of page views by desktop site from the Legacy Pagecounts API |
| pagecount_mobile_views | num_views      | the number of page views by mobile site from the Legacy Pagecounts API|
| pageview_all_views | num_views      |the number of all page views from the Pageviews API |
| pageview_desktop_views | num_views      | the number of page views by desktop from the Pageviews API|
| pageview_mobile_views | num_views      |the number of page views by mobile app and mobile web from the Pageviews API |

## Data Visualization

## Note
The Pageviews APT allows us to filter by agent=user data in order to exclude spiders/crawlers while the Pagecounts API does not.
The notebook uses Python version 3.7.4.
