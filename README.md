# Cambridge_MA_properties

I visualize and model some data from the Assessing Department of the City of Cambridge, MA, which is responsible for setting valuations of all real estate in the city. The study covers FY2016 to FY2018.

I obtained the data from the City's data archive. This particular set came from:

https://data.cambridgema.gov/Assessing/Cambridge-Property-Database-FY16-FY18/eey2-rv59

I don't want to proliferate stale data, so if you want to use this notebook, you should get the data from the City yourself at the link above. Then, just put the jupyter notebook in the same directory as the data CSV file, add a subdirectory called "output", and run the notebook.

Runnable notebooks in this repo include:
* Cambridge_property_mapping.ipynb: I do minimal processing to the data, and plot it on city maps in various ways. I used the MapboxGL library.
* Cambridge_property_ETLC.ipynb: Prior to modeling, I load and transform the data, and do quite a lot of cleaning to remove invalid values. Over 60% of the rows are affected by data entry errors, typified by a "frame shift"-like error in which a row starts out looking good, but then each column begins to get the value meant for the one before/after it, and the rest of the row is mostly bad data. I am imagining data entry into a spreadsheet, and not hitting Tab the right number of times.
* Cambridge_property_modeling.ipynb: Using the cleaned data, I make a reasonably accurate random forest model, then slice it several different ways to gain understanding of how the important features play into the model.

Two of these notebooks are supposed to contain a live map, but the map doesn't display correctly in Github's browser. To view it, download the notebook and run it. You can still see the various still images in the previewed notebooks.

On my wish-list: figure out how to export the live map to its own HTML document. At the moment, the create_html() method on the Mapbox GL library is not working for me; it displays the underlying map but not the data points.
