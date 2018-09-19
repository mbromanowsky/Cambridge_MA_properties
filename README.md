# Cambridge_MA_properties

I visualize some data from the Assessing Department of the City of Cambridge, MA, which is responsible for setting valuations of all real estate in the city. The study covers FY2016 to FY2018.

I obtained the data from the City's data archive. This particular set came from:

https://data.cambridgema.gov/Assessing/Cambridge-Property-Database-FY16-FY18/eey2-rv59

I don't want to proliferate stale data, so if you want to use this notebook, you should get the data from the City yourself at the link above. Then, just put the jupyter notebook in the same directory as the data CSV file, add a subdirectory called "output", and run the notebook.

The notebook is supposed to contain a live map, but it doesn't display correctly in Github's browser. To view it, download the notebook and run it. You can still see the various still images in the previewed notebook.

On my wish-list: figure out how to export the live map to its own HTML document. At the moment, the create_html() method on the Mapbox GL library is not working for me; it displays the underlying map but not the data points.
