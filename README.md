# Mars_Mission

This project called "Mars Mission" uses Pandas to scrape the table containing facts about the planet including Diameter, Mass, and show them on HTML page.
The project visits the USGS Astrogeology site to obtain high resolution images for each of Mars hemispheres.
It uses Python dictionary to store the data using the keys img_url and title.
# Example:
hemisphere_image_urls = [
    {"title": "Valles Marineris Hemisphere", "img_url": "..."},
    
    {"title": "Cerberus Hemisphere", "img_url": "..."},
    
    {"title": "Schiaparelli Hemisphere", "img_url": "..."},
    
    {"title": "Syrtis Major Hemisphere", "img_url": "..."},
]



Step 2 - MongoDB and Flask Application

The project uses MongoDB with Flask templating to create a new HTML page that displays all of the information that was scraped from the URLs above.

This started by converting Jupyter notebook into a Python script called scrape_mars.py with a function called scrape that execute all of scraping code from above and return one Python dictionary containing all of the scraped data.

Next, the project creates a route called /scrape that imported scrape_mars.py script and called scrape function.

The project creates also a root route / that query Mongo database and pass the mars data into an HTML template to display the data.
Also it creates template HTML file called index.html that takes the mars data dictionary and display all of the data in the appropriate HTML elements. 
