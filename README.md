# Mars_Mission

Complete your initial scraping using Jupyter Notebook, BeautifulSoup, Pandas, and Requests/Splinter.


Create a Jupyter Notebook file called mission_to_mars.ipynb and use this to complete all of your scraping and analysis tasks. The following outlines what you need to scrape.



NASA Mars News


Scrape the NASA Mars News Site and collect the latest News Title and Paragraph Text. Assign the text to variables that you can reference later.


# Example:
news_title = "NASA's Next Mars Mission to Investigate Interior of Red Planet"

news_p = "Preparation of NASA's next spacecraft to Mars, InSight, has ramped up this summer, on course for launch next May from Vandenberg Air Force Base in central California -- the first interplanetary launch in history from America's West Coast."

JPL Mars Space Images - Featured Image


Visit the url for JPL Featured Space Image here.
Use splinter to navigate the site and find the image url for the current Featured Mars Image and assign the url string to a variable called featured_image_url.
Make sure to find the image url to the full size .jpg image.
Make sure to save a complete url string for this image.


# Example:
featured_image_url = 'https://www.jpl.nasa.gov/spaceimages/images/largesize/PIA16225_hires.jpg'

Mars Weather


Visit the Mars Weather twitter account here and scrape the latest Mars weather tweet from the page. Save the tweet text for the weather report as a variable called mars_weather.


# Example:
mars_weather = 'Sol 1801 (Aug 30, 2017), Sunny, high -21C/-5F, low -80C/-112F, pressure at 8.82 hPa, daylight 06:09-17:55'

Mars Facts


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
