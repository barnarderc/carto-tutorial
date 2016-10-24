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

Carto's platform divides users' accounts into a **Datasets** tab and a ***Map*** tab. In the Datasets tab, users can upload, edit, view or delete their own datasets. In the map view, users are able to build interactive mapping projects, combining one or more of their own datasets, to be published or shared. 

![](https://github.com/barnarderc/carto-tutorial/blob/master/images/map-datasets-view.JPG?raw=true)

In order to begin mapping the data for this tutorial, we must first upload our dataset to Carto. The data we will be using is in a tabular format, representing location points for a group of people as they travel from a starting location to Paris, France. Here is a peek at the data structure: 

![](https://github.com/barnarderc/carto-tutorial/blob/master/images/data-descrip.JPG?raw=true)

The data is formatted with 7 columns:
-	`person`: Person in the dataset's name, identifying who was at the given location point
-	`sequence`: Number of the sequence in which the given person stopped at the location point (if 1, then row represents the person's first stop, if 2, represents their second stop, etc.)
-	`lat`: Number representing the latitude; is one half of the location information necessary to plot the points in Carto. 
-	`lon`: Number representing the longitude; second half of the location information necessary to plot the points in Carto. 
-	`location`: Name of the city, if given, of the person's location
-	`country`: Name of the country, of location
-	`id`: Unique id for each person, to identify who was at given location







