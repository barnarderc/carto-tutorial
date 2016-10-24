# Introduction to Mapping with Carto 

####Workshop Objectives 
This exercise is intended to introduce users to mapping and displaying spatial information using the online platform, Carto. 

[Carto](https://carto.com) is an online platform that allows users to upload data and provides tools to visualize that data in interactive maps. Maps made on Carto can be shared and embeded on websites and in different formats. On of the advantages of using Carto as opposed to other interactive mapping platforms is that it allows you to directly upload your datasets and manipulate them online. This functionality includes selecting certain specific parts of your dataset using SQL-style queries. 

In this first introductory tutorial users will:

1. Create a Carto account
1. Become familiar with Carto's dataset and map views
1. Learn how to upload simple datasets in tabular and vector formats to their Carto account
1. Learn basics of interface and visualization tools 


Subsequent tutorial pages demonstrate how to execute simple data manipulations in Carto, as well as add interactive elements, customize basemaps, and embed and share maps.

The data used in this workshop can be found in the data folder of this repository [(here)](https://github.com/barnarderc/carto-tutorial/tree/master/data). 

- - - -
####Creating a Carto Account

To begin using Carto, users must first create an online account [here](https://carto.com/signup). Carto's basic account is free, and allows users to upload a limited number of files. 

Once you've created your account, and verified your email, when you sign into Carto you will be presented with the option to begin by creating a new map. 

![Intro page](https://github.com/barnarderc/carto-tutorial/blob/master/images/create-account.JPG?raw=true)

- - - 

#### Becoming Familiar with Carto's Interface 

Carto's platform divides users' accounts into a **Datasets** tab and a ***Map** tab. In the Datasets tab, users can upload, edit, view or delete their own datasets. In the map view, users are able to build interactive mapping projects, combining one or more of their own datasets, to be published or shared. 

![](https://github.com/barnarderc/carto-tutorial/blob/master/images/map-datasets-view.JPG?raw=true)

We will begin using Carto by uploading our dataset, **carto-tutorial-data.csv** from the **data** folder. Before we upload this data to Carto, let's take a look at how it is formatted. 

- - - 

The data we will be using is in a tabular format, representing location points for three people as they travel from different starting locations, and end up in Paris, France. Here is a peek at the data structure: 


The data is formatted with 7 columns:
-	`person`: Person in the dataset's name, identifying who was at the given location point
-	`sequence`: Number of the sequence in which the given person stopped at the location point (if 1, then row represents the person's first stop, if 2, represents their second stop, etc.)
-	`lat`: Number representing the latitude; is one half of the location information necessary to plot the points in Carto. 
-	`lon`: Number representing the longitude; second half of the location information necessary to plot the points in Carto. 
-	`location`: Name of the city, if given, of the person's location
-	`country`: Name of the country, of location
-	`id`: Unique id for each person, to identify who was at given location


![](https://github.com/barnarderc/carto-tutorial/blob/master/images/data-descrip.JPG?raw=true)


Each of the three people has 7 location stops, as they make their way around the world to Paris. Each row represents one stop. In this tutorial, we are interested in mapping these individuals' movement, following their sequence of stops. We do not have any information about how much time they spend in each stop, but we do know the order they travel based on the `sequence` column. We also know which person stops where because we have an `id` column and a column with their name (`person`). 

Now that we have an idea of what our data looks like, and what we are interested in mapping, we can upload the dataset to Carto and begin to explore and visualize it. 

- - - 

On the Carto web page, navigate to the "Your Datasets" tab, and click on the "New Dataset" option on the right-hand side of the page. A new window will appear, prompting users to choose the way in which to connect their dataset. 

![](https://github.com/barnarderc/carto-tutorial/blob/master/images/carto-upload-dataset.JPG?raw=true)

Users are able to connect datasets from a variety of sources, including data hosted on Google Drive and Dropbox. Users can also upload data in a variety of formats, tabular but also geographic. 

In this case we have our **carto-tutorial-data.csv**, which you should download, and which we will upload by browsing to its downloaded location on your local computer. 

Once chosen, connect the data by clicking "Connect Dataset". 

- - - 

When the data is finished uploading, Carto will open the dataset and you should see the same rows and columns as shown previously. One main difference that should be noted, is that Carto has added a column `the_geom`. This column tells Carto how to map the points, and is based off of our `lat` and `lon` columns. Carto has also added a column called `cartodb_id`; this is just a column with unique numbers for each row. 

From here, we can go ahead and display this data on a map. At the top of the table, there is a sliding icon, which currently shows that we are in **Data View**. Toggle the slider to **Map View**. 

![](https://github.com/barnarderc/carto-tutorial/blob/master/images/map-view-1.JPG?raw=true)

