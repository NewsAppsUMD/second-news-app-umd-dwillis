# Second news app

A step-by-step guide to publishing a simple news application.

* Demonstration: [http://ireapps.github.io/first-news-app/build/index.html](http://ireapps.github.io/first-news-app/build/index.html)
* Documentation: [https://first-news-app-umd.readthedocs.io/en/latest/](https://first-news-app-umd.rtfd.org)
* Issues: [https://github.com/NewsAppsUMD/first-news-app-umd/issues](https://github.com/NewsAppsUMD/first-news-app-umd/issues)

Zip code boundaries:

https://data.imap.maryland.gov/datasets/38f3f8bc61bb4261b59d71b3642e3cd6_3/explore?location=38.802898%2C-77.268250%2C8.83

* go to mapbox and sign up for free account, generate access token
* Download geojson, move to static folder and rename to md_zips.geojson
* pip install geojson
* create maps.py and copy in script to split into individual geojson files for each zip
* run maps.py
* delete md_zips.geojson
* in app.py, create geojson_url in detail function & pass it to template
* in detail.html, add MapBox js/css and Turf.js js to head
* copy and paste map code into detail.html
* run server and load a zip code


Better homepage

* Add Flask imports to app.py and set secret key.
* Update index() function to accept GET & POST requests and look for a zip code submitted by the form
* Replace index.html template with index_new version
* Add top zip codes in March 2023
* Add sentence to detail to determine if the March 2023 figure is the most ever