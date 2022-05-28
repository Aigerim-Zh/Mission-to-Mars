# Mission-to-Mars

# Project Overview

In this project, I am tasked with web scraping data from active NASA websites to gather Mars information on:
* Latest News 
* Featured Image
* Mars Facts
* Hemisphere Images

The web scraping process developed in this project gathers these data from different sources quickly instead of visiting each website and manually extracting the data. The process is automated using a programming script. 

# Data and Resources
* ```Chrome Developer Tool``` to identify HTML and CSS components
* Extracting data with ```BeatifulSoup``` 
* Automating web scraping with ```Splinter``` 
* Programming code using ```Python 3.9.2``` through ```Jupyter Notebook```
* Parsing HTML in Python using ```html5lib``` and ```lxml``` libraries.
* Creating a web application using ```Flask```
* Customizing the web application using ```HTML```, ```CSS```, and ```Bootstrap 3```
* ```MongoDB``` is a choice for this project because the data I will be scraping from the web is not going to be uniform. To be more precise, Mongo will store and access images as a document, which SQL is not capable of. 

# Results 

## Deliverable 1
First, I created a web-scraping code in Jupyter Notebook [Mission_to_Mars_Challenge.ipynb](https://github.com/Aigerim-Zh/Mission-to-Mars/blob/main/Challenge/Mission_to_Mars_Challenge.ipynb) extracting:
* The most recent news article along with its summary on Mars facts from NASA's [MARS Exploration Program](https://redplanetscience.com).
* Featured image (most recently posted) from the Jet Propulsion Laboratory's [Space Images](https://spaceimages-mars.com) webpage. 
* Table with a collection of Mars facts from https://galaxyfacts-mars.com/. 
* Images of Mars hemispheres and titles from https://marshemispheres.com/.

## Deliverable 2
Next, I converted the Jupyter Notebook file into a Python file, [Mission_to_Mars_Challenge.py](https://github.com/Aigerim-Zh/Mission-to-Mars/blob/main/Challenge/Mission_to_Mars_Challenge.py) and prepared the final application code, [app.py](https://github.com/Aigerim-Zh/Mission-to-Mars/blob/main/Challenge/app.py), which
- connects to the Mongo database. 
- has a route that reproduces the following template: [index.html](https://github.com/Aigerim-Zh/Mission-to-Mars/blob/main/Challenge/templates/index.html).
- has a scraping route using the [scraping.py]() file, which modifies the scraping process from [Mission_to_Mars_Challenge.py](https://github.com/Aigerim-Zh/Mission-to-Mars/blob/main/Challenge/Mission_to_Mars_Challenge.py) with functions for each scrape. 

After running the web application, this is the initial web page view:

![](https://github.com/Aigerim-Zh/Mission-to-Mars/blob/main/Challenge/Images/Initial_web_view.png)

## Deliverable 3 
Next, the web page's mobile responsiveness was ensured. 

Here is a view from **iPhone12 Pro**:

![](https://github.com/Aigerim-Zh/Mission-to-Mars/blob/main/Challenge/Images/View_from_iPhone12Pro.png)

Here is a view from **iPad Air**:

![](https://github.com/Aigerim-Zh/Mission-to-Mars/blob/main/Challenge/Images/View_from_iPadAir.png)

Lastly, the following **additional Bootstrap 3 components** were implemented to customize the view of the web page:

1. Adding a theme image to the header background:
```
   <div class="jumbotron text-center" style="background-image: url(https://mars.nasa.gov/system/news_items/main_images/8944_1-PIA24546-1280.jpg);">
```

![](https://github.com/Aigerim-Zh/Mission-to-Mars/blob/main/Challenge/Images/Updated_header.png)

2. Making hemisphere images as thumbnails by changing the grid from ```<div class="col-md-6">``` to ```<div class="col-md-3">```. Thumbnails are smaller versions of full digital images that can easily be viewed when browsing a web page with several images. 

![](https://github.com/Aigerim-Zh/Mission-to-Mars/blob/main/Challenge/Images/Hemisphere_images_as_thumbnails.png)

3. Changing the web page background color to grey. 

```
<body style="background-color:grey; color:black">
```

![](https://github.com/Aigerim-Zh/Mission-to-Mars/blob/main/Challenge/Images/Updated_background.png)
