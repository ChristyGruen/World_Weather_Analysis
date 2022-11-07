#  <span style="color:tan"> **Module 6 API Challenge**  </span>
### Chris Gruenhagen 7Nov2022
Homework Log

The WeatherPy and VacationPy homework is located in the "WeatherPy_VacationPy" directory in the python-api-challenge repository.  The WeatherPy homework consists of a jupyter notebook "WeatherPy.ipynb" and output files located in the "output_data" directory.  The VacationPy homework consists of a jupyter notebook "VacationPy.ipynb"

**Homework Summary**


## Part 1: Weather Py
---
### **Purpose**

The purpose of this study was to provide comprehensive data to answer a fundamental question:  What is the weather like as we approach the equator?

### **Study Format**

In this study, data on a single day (Nov 6, 2022) from over 500 random cities of varying distances from the equator were evaluated to visualize the potential relationships between latitude and temperature, humidity, cloudiness, and wind speed in both the Northern and Southern hemispheres. Data was obtained from OpenWeather https://openweathermap.org/.

Limitations:  This dataset was generated on a single day so it does not capture day to day variation, and it relies on data from cities which are generally located in more liveable locations by latitude.  Comparisons between the northern and southern hemispheres may be impacted by differences in the number of cities (northern = 393, southern = 168) and ranges of latitude evaluated (northern 0 to 77, southern 0 to -55).

Exclusions: At the beginning of the study, 611 random cities were selected from the citipy library. While pulling additional weather data from OpenWeather, 50 cities were excluded due to errors in data processing, leaving a dataset of 561 cities for analysis.

### **Attribution**
‘Weather data provided by OpenWeather’
https://openweathermap.org/

Powered by https://www.geoapify.com/ Geoapify

Powered by https://www.openstreetmap.org/copyright © OpenStreetMap contributors

R correlation matrix: https://sphweb.bumc.bu.edu/otlt/MPH-Modules/PH717-QuantCore/PH717-Module9-Correlation-Regression/PH717-Module9-Correlation-Regression4.html

### Conclusions

What is the weather like as we approach the equator?

Based on the data collected on 561 random cities on November 6, 2022 from OpenWeather https://openweathermap.org/, temperature increases and wind speed appears to decrease as we approach the equator.  Humidity and cloudiness did not appear to be correlated with latitude.

### **Analysis**
### *Requirement 1:  Create Plots to showcase the relationship between weather variables and latitude across the globe.*

Worldwide Latitude vs Temperature
![Alt text](/WeatherPy_VacationPy/output_data/Fig1.png "Latitude vs Temp")

Worldwide Latitude vs Humidity
![Alt text](/WeatherPy_VacationPy/output_data/Fig2.png "Latitude vs Humidity")

Worldwide Latitude vs Cloudiness
![Alt text](/WeatherPy_VacationPy/output_data/Fig3.png "Latitude vs Cloudiness")

Worldwide Latitude vs Wind Speed

![Alt text](/WeatherPy_VacationPy/output_data/Fig4.png "Latitude vs Wind Speed")
---
### *Requirement 2: Compute Linear Regression for Each Relationship in the Northern and Southern Hemispheres.*

Latitude vs Temperature in the Northern and Southern Hemispheres
![Alt text](/WeatherPy_VacationPy/output_data/North_Lat_vs_Max%20Temp.png "Northern Latitude vs Humidity")
![Alt text](/WeatherPy_VacationPy/output_data/South_Lat_vs_Max%20Temp.png "Southern Latitude vs Humidity")

        **Discussion about the linear relationship:**
         In the northern hemisphere, there is a very strong negative correlation (r = -0.84) between latitude and max temperature.  In the southern hemisphere, there is a moderate correlation (r = 0.53) between latitude and max temperature.  In both hemispheres, the max temperature increases as you approach the equator (latitude = 0). 
         
         The northern latitude appears to have a greater temperature difference (-33C to 33C) than the southern latitude (9C to 33C), but the city locations in the northern latitudes also span a much greater range of latitudes (lat 0 to 77) than the cities in the southern latitudes (lat 0 to -55). Additional data and/or analysis would be required to evaluate differences between the two hemispheres.
         


Latitude vs Humidity in the Northern and Southern Hemispheres
![Alt text](/WeatherPy_VacationPy/output_data/North_Lat_vs_Humidity.png "Northern Hemisphere Latitude vs Humidity") 
![Alt text](/WeatherPy_VacationPy/output_data/South_Lat_vs_Humidity.png "Southern Hemisphere Latitude vs Humidity")

        **Discussion about the linear relationship:** 
        In the northern hemisphere, there is a very weak to weak correlation (r = 0.24) between latitude and humidity. In the southern hemisphere, there is a weak correlation (r =0.32) between latitude and humidity.  Humidity varies widely across latitudes in both hemispheres, from 13 to 100%. 

Latitude vs Cloudiness in the Northern and Southern Hemispheres
![Alt text](/WeatherPy_VacationPy/output_data/North_Lat_vs_Cloudiness.png "Northern Hemisphere Latitude vs Cloudiness") 
![Alt text](/WeatherPy_VacationPy/output_data/South_Lat_vs_Cloudiness.png "Southern Hemisphere Latitude vs Cloudiness")

        **Discussion about the linear relationship:** 
        In both the northern and southern hemispheres, there is a weak correlation (r = 0.28, r = 0.33) between latitude and cloudiness. Cloudiness varies widely across latitudes in both hemispheres, from 0 to 100%.

Latitude vs Wind Speed in the Northern and Southern Hemispheres
![Alt text](/WeatherPy_VacationPy/output_data/North_Lat_vs_Wind%20Speed.png "Northern Hemisphere Latitude vs Wind Speed") 
![Alt text](/WeatherPy_VacationPy/output_data/South_Lat_vs_Wind%20Speed.png "Southern Hemisphere Latitude vs Wind Speed")

        **Discussion about the linear relationship:** 
        In the northern hemisphere, there is a very weak to weak correlation (r = 0.22) between latitude and wind speed. In the southern hemisphere, there is a weak negative correlation (r = - 0.29) between latitude and wind speed.  Although wind speed varies widely across latitudes in both hemispheres (0-14 m/s), the average wind speed in both hemispheres appear to decrease as you approach the equator (latitude = 0).

## Part 2: Vacation Py
---
### Purpose

The purpose of this study was to provide weather and hotel information for cities across the globe to aid in planning future vacations. 

### Study Format

In this study, data on a single day (Nov 6, 2022) from over 500 random cities of varying distances from the equator were evaluated to visualize the weather and hotel information on a world map. Weather information was evaluated to provide hotel locations with ideal weather conditions. Data was obtained from OpenWeather https://openweathermap.org/,  Geoapify https://www.geoapify.com/ and © OpenStreetMap contributors https://www.openstreetmap.org/copyright .

Limitations:  This dataset was generated on a single day so it does not capture day to day variation.

### **Attribution**
‘Weather data provided by OpenWeather’
https://openweathermap.org/

Powered by https://www.geoapify.com/ Geoapify

Powered by https://www.openstreetmap.org/copyright © OpenStreetMap contributors

### Conclusion
Of the 561 cities evaluated, six cities met the ideal weather conditions (max temp 70-90C, wind speed <10 m/s, cloudiness <25%, humidity 30-50%) and had a hotel located within 10,000 meters of the city coordinates.

| City |Country|Hotel|
| --- | --- | --- |
|molina|CL|La Cabaña|
|diamantino|BR|Hotel kayaby|
|santa luzia|BR|Alcoboca|
|odweyne|SO|فندق المدينه|
|ariquemes|BR|Aquarius|
|santa rosalia|MX|Hotel del Real|



### Analysis
The cities data gathered in the WeatherPy excercise (n = 561) was used to create a map visualizing the city location and humidity.   

![Alt text](/WeatherPy_VacationPy/AllCities%20VacationPy%202022-11-06.png "City Location and Humidity")

The cities data was further filtered by the following ideal conditions: 
* Max Temperature between 70 to 90 degrees Fahrenheit
* Wind speed less than 10 meters/second
* Cloudiness less than 25% 
* Humidity between 30% and 50% 
For each ideal city (n = 8), Geoapify was used to find the first hotel located within 10,000 meters of the city coordinates. The query found six of the cities with hotels within range and two of the cities without hotels within range.

![Alt text](/WeatherPy_VacationPy/IdealCities%20VacationPy%202022-11-06 .png "Ideal Cities and Hotels")




# &#x1F31E; &#x26C5; &#x2601; &#x1F327; &#x1F308; &#x1F327; &#x2601; &#x26C5; &#x1F31E;





     emoji & format references:
        https://emojipedia.org
        https://www.markdownguide.org/basic-syntax/
        https://stackoverflow.com/questions/35465557/how-to-apply-color-on-text-in-markdown
        https://stackoverflow.com/questions/6046263/how-to-indent-a-few-lines-in-markdown-markup

***See below for original homework instructions***
# <span style="color:tan"> Module 6 Challenge </span>
Due Nov 7 by 11:59pm 

Points 100 

Submitting a text entry box or a website url
_________________________________________________________
## <span style="color:red"> **Background**  </span>
Data's true power is its ability to definitively answer questions. So, let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"

Now, we know what you may be thinking: “That’s obvious. It gets hotter.” But, if pressed for more information, how would you prove that?

##  <span style="color:orange"> **Before You Begin** </span>
Create a new repository for this project called python-api-challenge. Do not add this homework to an existing repository.

Clone the new repository to your computer.

Inside your local Git repository, create a directory for this assignment. Use a folder name that corresponds to the Challenges, such as WeatherPy.

Inside the folder you just created, add the files called WeatherPy.ipynb and VacationPy.ipynb that you will find in the starter code ZIP file provided. These will be the main scripts to run for each analysis.

Push your changes to GitHub.
### ***Add a .gitignore File***
For this assignment, you will need to add a .gitignore file to your repo. This is so you don’t expose the api_keys.py file with your API key to the public, which would allow anyone using GitHub to copy and use your API key, possibly incurring charges.

When you type git status in the command line, you’ll get a list of all the untracked files that you have created so far.

If you wanted to add only the WeatherPy.ipynb file to GitHub, you would type git add WeatherPy.ipynb. However, whenever you want to add or update a file, you would have to add each file individually, which is time-consuming and cumbersome. Instead, you can add the files that you don't want to track to the .gitignore file.

Before adding your files to GitHub, add api_keys.py to the .gitignore file by following these steps:

Open your python-api-challenge GitHub folder in VS Code.

Open the .gitignore file, and on the first line, type the following code:

        # Adding config.py file.
        api_keys.py
While the .gitignore file is open, add the API_practice.ipynb and random_numbers.ipynb files and save the file.

In the command line, type git status and press Enter. The output should indicate that the .gitignore file has been modified and the WeatherPy.ipynb file is untracked.

Use git add, git commit, and git push to commit the modifications to .gitignore and the WeatherPy.ipynb file to GitHub.

On GitHub, the only new file you should find is the WeatherPy.ipynb file.

##  <span style="color:yellow"> **Files** </span>
Download the following files to help you get started:

Module 6 Challenge files

https://courses.bootcampspot.com/courses/2584/files/2120444/download

##  <span style="color:green">  **Instructions** </span>
This activity is broken down into two parts, WeatherPy and VacationPy.

### ***Part 1: WeatherPy***
In this section, you'll create a Python script to visualize the weather of over 500 cities of varying distances from the equator. You'll use a simple 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; citypy Python library

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; https://pypi.python.org/pypi/citipy, 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; the OpenWeatherMap API 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; https://openweathermap.org/api, 

and your problem-solving skills to create a representative model of weather across cities.
For this part, you'll use the WeatherPy.ipynb Jupyter notebook provided in the starter code ZIP file. The starter code will guide you through the process of using your Python coding skills to develop a solution to address the required functionalities.

To get started, the code required to generate random geographic coordinates and the nearest city to each latitude and longitude combination is provided.

#### **Requirement 1: Create Plots to Showcase the Relationship Between Weather Variables and Latitude**
To fulfill the first requirement, you'll use the OpenWeatherMap API to retrieve weather data from the cities list generated in the starter code. Next, you'll create a series of scatter plots to showcase the following relationships:

* Latitude vs. Temperature
* Latitude vs. Humidity
* Latitude vs. Cloudiness
* Latitude vs. Wind Speed

#### **Requirement 2: Compute Linear Regression for Each Relationship**
To fulfill the second requirement, compute the linear regression for each relationship. Separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude). You may find it helpful to define a function in order to create the linear regression plots.

Next, create a series of scatter plots. Be sure to include the linear regression line, the model's formula, and the r values.

You should create the following plots:

* Northern Hemisphere: Temperature vs. Latitude
* Southern Hemisphere: Temperature vs. Latitude
* Northern Hemisphere: Humidity vs. Latitude
* Southern Hemisphere: Humidity vs. Latitude
* Northern Hemisphere: Cloudiness vs. Latitude
* Southern Hemisphere: Cloudiness vs. Latitude
* Northern Hemisphere: Wind Speed vs. Latitude
* Southern Hemisphere: Wind Speed vs. Latitude

After each pair of plots, explain what the linear regression is modeling. Describe any relationships that you notice and any other findings you may uncover.

Your final notebook must meet the following requirements:

Randomly select at least 500 unique (not repeated) cities based on latitude and longitude.

Perform a weather check on each of the cities by using a series of successive API calls.

Include a print log of each city as it's being processed, with the city number and city name.

Save a CSV of all retrieved data and a PNG image for each scatter plot.

### ***Part 2: VacationPy***
In this deliverable, you'll use your weather data skills to plan future vacations. Also, you'll use Jupyter notebooks, the geoViews Python library, and the Geoapify API.
The code needed to import the required libraries and load the CSV file with the weather and coordinates data for each city created in Part 1 is provided to help you get started.Your main tasks will be to use the Geoapify API and the geoViews Python library and employ your Python skills to create map visualizations.

To succeed on this deliverable of the assignment, open the VacationPy.ipynb starter code and complete the following steps:

1. Create a map that displays a point for every city in the city_data_df DataFrame as shown in the following image. The size of the point should be the humidity in each city.
2. Narrow down the city_data_df DataFrame to find your ideal weather condition. For example:
* A max temperature lower than 27 degrees but higher than 21
* Wind speed less than 4.5 m/s
* Zero cloudiness

**NOTE**
Feel free to adjust your specifications but make sure to set a reasonable limit to the number of rows returned by your API requests.

3. Create a new DataFrame called hotel_df to store the city, country, coordinates, and humidity.

4. For each city, use the Geoapify API to find the first hotel located within 10,000 meters of your coordinates.

5. Add the hotel name and the country as additional information in the hover message for each city on the map.

##  <span style="color:blue"> **Hints and Considerations** </span>
* The city data that you generate is based on random coordinates and different query times, so your outputs will not be an exact match to the provided starter notebook.

* If you'd like a refresher on the geographic coordinate system, this siteLinks to an external site. has great information.

* Take some time to study the OpenWeatherMap API. Based on your initial study, you should be able to answer basic questions about the API: Where do you request the API key? Which Weather API in particular will you need? What URL endpoints does it expect? What JSON structure does it respond with? Before you write a line of code, you should have a crystal-clear understanding of your intended outcome.

* A starter code for citipy has been provided. However, if you're craving an extra challenge, push yourself to learn how it works by using the citipy Python libraryLinks to an external site.. Before you try to incorporate the library in your analysis, start with simple test cases outside of your main script to confirm that you are using it correctly. Often, when introduced to a new library, learners spend hours trying to figure out errors in their code when a simple test case can save you a lot of time and frustration.

* You will need to apply your critical thinking skills to understand how and why we're recommending these tools. What is citipy used for? Why would you use it in conjunction with the OpenWeatherMap API? How would you do so?

* While building your script, pay attention to the cities you are using in your query pool. Are you covering the full range of latitudes and longitudes? Or are you choosing 500 cities from one region of the world? Even if you were a geography genius, simply listing 500 cities based on your personal selection would create a biased dataset. Try to think of ways that you can counter these selection issues.

Hint: Consider the full range of latitudes.
* Once you have computed the linear regression for one relationship, you will follow a similar process for all other charts. As a bonus, try to create a function that will create these charts based on different parameters.

* Remember that each coordinate will trigger a separate call to the Google API. If you're creating your own criteria to plan your vacation, try to reduce the results in your DataFrame to 10 or fewer cities.

* Ensure that your repository has regular commits and a thorough README.md file.

* Lastly, remember that this is a challenging activity. Push yourself! If you complete this task, you can safely say that you've gained a strong understanding of the core foundations of data analytics, and it will only get better from here. Good luck!

## <span style="color:indigo"> **Requirements**  </span>
#### **The requirements for "Part 1: WeatherPy" are the following**
Create Plots to Showcase the Relationship Between Weather Variables and Latitude (30 points)
* Use the OpenWeatherMap API to retrieve weather data from the cities list generated in the started code (10 points)
* Create a scatter plot to showcase the relationship between Latitude vs. Temperature (5 points)
* Create a scatter plot to showcase the relationship between Latitude vs. Humidity (5 points)
* Create a scatter plot to showcase the relationship between Latitude vs. Cloudiness (5 points)
* Create a scatter plot to showcase the relationship between Latitude vs. Wind Speed (5 points)

Compute Linear Regression for Each Relationship (40 points)
* Linear regression scatter plot for Northern Hemisphere: Temperature (C) vs. Latitude (5 points)
* Linear regression scatter plot for Southern Hemisphere: Temperature (C) vs. Latitude (5 points)
* Linear regression scatter plot for Northern Hemisphere: Humidity (%) vs. Latitude (5 points)
* Linear regression scatter plot for Southern Hemisphere: Humidity (%) vs. Latitude (5 points)
* Linear regression scatter plot for Northern Hemisphere: Cloudiness (%) vs. Latitude (5 points)
* Linear regression scatter plot for Southern Hemisphere: Cloudiness (%) vs. Latitude (5 points)
* Linear regression scatter plot for Northern Hemisphere: Wind Speed (m/s) vs. Latitude (5 points)
* Linear regression scatter plot for Southern Hemisphere: Wind Speed (m/s) vs. Latitude (5 points)

#### **The requirements for "Part 2: VacationPy" are the following (30 points)**
* Create a map that displays a point for every city in the city_data_df DataFrame (5 points)
* Narrow down the city_data_df DataFrame to find your ideal weather condition (5 points)
* For each city in the hotel_df DataFrame, use the Geoapify API to find the first hotel located within 10,000 metres of your coordinates (10 points)
* Add the hotel name and the country as additional information in the hover message for each city in the map. (10 points)


## <span style="color:Violet"> **Submission**  </span>
To submit your Challenge assignment, click Submit, and then provide the URL of your GitHub repository for grading.

>**NOTE**

You are allowed to miss up to two Challenge assignments and still earn your certificate. If you complete all Challenge assignments, your lowest two grades will be dropped. If you wish to skip this assignment, click Next, and move on to the next module.

Comments are disabled for graded submissions in Bootcamp Spot. If you have questions about your feedback, please notify your instructional staff or your Student Success Manager. If you would like to resubmit your work for an additional review, you can use the Resubmit Assignment button to upload new links. You may resubmit up to three times for a total of four submissions.


>**NOTE**

Remember that any API usage beyond the $200 credit will be charged to your personal account. You can set quotas and limits to your daily requests to be sure that you won’t be charged. Check out 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Google Maps Platform Billing

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;https://developers.google.com/maps/billing/gmp-billing#monitor-and-restrict-consumption

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Manage your cost of use

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;https://developers.google.com/maps/documentation/javascript/usage-and-billing#set-caps

for more information.

## <span style="color:Tan"> **References** </span>
© 2020 - 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.