#  <span style="color:tan"> **Module 6 API Challenge**  </span>
### Chris Gruenhagen DATE
Homework Log

The WeatherPy and VacationPy homework is located in the "WeatherPy_VacationPy" directory in the python-api-challenge repository.  The WeatherPy homework consists of a jupyter notebook "WeatherPy.ipynb" and output files located in the "output_data" directory.  The VacationPy homework consists of a jupyter notebook "VacationPy.ipynb"

**Homework Summary**


## Part 1: Weather Py
---
### **Purpose**

The purpose of this study was to provide comprehensive data to answer a fundamental question:  What is the weather like as we approach the equator?

### **Study Format**

In this study, over 500 random cities of varying distances from the equator were evaluated to visualize the potential relationships between latitude and temperature, humidity, cloudiness, and wind speed in both the Northern and Southern hemispheres. Data was obtained from OpenWeather https://openweathermap.org/.  

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
         In the northern hemisphere, there is a very strong negative correlation (r = -0.84) between latitude and max temperature.  In the southern hemisphere, there is a strong correlation (r = 0.68) between latitude and max temperature.  In both hemispheres, the max temperature increases as you approach the equator (latitude = 0).  


Latitude vs Humidity in the Northern and Southern Hemispheres
![Alt text](/WeatherPy_VacationPy/output_data/North_Lat_vs_Humidity.png "Northern Hemisphere Latitude vs Humidity") 
![Alt text](/WeatherPy_VacationPy/output_data/South_Lat_vs_Humidity.png "Southern Hemisphere Latitude vs Humidity")

        **Discussion about the linear relationship:** 
        In the northern hemisphere, there is a weak to moderate correlation (r = 0.36) between latitude and humidity. In the southern hemisphere, there is no  correlation (r =0.12) between latitude and humidity.  Although humidity varies widely across latitudes in both hemispheres, the average humidity in the northern hemisphere appears to increase with latitude.

Latitude vs Cloudiness in the Northern and Southern Hemispheres
![Alt text](/WeatherPy_VacationPy/output_data/North_Lat_vs_Cloudiness.png "Northern Hemisphere Latitude vs Cloudiness") 
![Alt text](/WeatherPy_VacationPy/output_data/South_Lat_vs_Cloudiness.png "Southern Hemisphere Latitude vs Cloudiness")

        **Discussion about the linear relationship:** 
        In the northern hemisphere, there is a very weak correlation (r = 0.2) between latitude and cloudiness.  In the southern hemisphere, there is a very weak (r =0.24) between latitude and cloudiness.  Cloudiness varies widely across latitudes in both hemispheres, from 0 to 100%.

Latitude vs Wind Speed in the Northern and Southern Hemispheres
![Alt text](/WeatherPy_VacationPy/output_data/North_Lat_vs_Wind%20Speed.png "Northern Hemisphere Latitude vs Wind Speed") 
![Alt text](/WeatherPy_VacationPy/output_data/South_Lat_vs_Wind%20Speed.png "Southern Hemisphere Latitude vs Wind Speed")

        **Discussion about the linear relationship:** 
        In the northern hemisphere, there is no correlation (r = 0.10) between latitude and wind speed. In the southern hemisphere, there is a weak negative correlation (r = - 0.28) between latitude and wind speed.  Although wind speed varies widely across latitudes in both hemispheres (0-16 m/s), the average wind speed in the southern hemisphere appears to increase with latitude.


### Conclusions

What is the weather like as we approach the equator?
Based on the data collected on over 500 random cities on November 6, 2022 from OpenWeather https://openweathermap.org/, temperature increases and wind speed appears to decrease as we approach the equator.  Humidity and cloudiness did not appear to be correlated with latitude.  


## Part 2: Vacation Py
---
### Purpose

The purpose of this study was to provide weather and hotel information for cities across the globe to aid in planning future vacations. 

### Study Format

In this study, over 500 random cities of varying distances from the equator were evaluated to visualize the weather and hotel information on a world map. Weather information was evaluated to provide hotel locations with ideal weather conditions (as defined by the user). Data was obtained from OpenWeather https://openweathermap.org/,  Geoapify https://www.geoapify.com/ and © OpenStreetMap contributors https://www.openstreetmap.org/copyright .

### Analysis
The cities data gathered in the WeatherPy excercise was used to create a map visualizing the city location and humidity.   

The cities data was further filtered by the following ideal conditions: 
* Max Temperature between 70 to 90 degrees Fahrenheit
* Wind speed less than 10 meters/second
* Cloudiness less than 25% 
* Humidity between 30% and 50% 
For each ideal city, Geoapify was used to find the first hotel located within 10,000 meters of the city coordinates.




TBD


### Exclusions
TBD - or delete




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

Inside the folder you just created, add new files called WeatherPy.ipynb and VacationPy.ipynb. These will be the main scripts to run for each analysis.

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

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Python library

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; https://pypi.python.org/pypi/citipy, 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; the OpenWeatherMap API 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; https://openweathermap.org/api, 

and your problem-solving skills to create a representative model of weather across cities.

The first requirement is to create a series of scatter plots to showcase the following relationships:

Temperature (F) vs. Latitude

Humidity (%) vs. Latitude

Cloudiness (%) vs. Latitude

Wind Speed (mph) vs. Latitude

After each plot, add one to two sentences to explain what the code is analyzing.

The second requirement is to compute the linear regression for each relationship. This time, separate the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

Northern Hemisphere: Temperature (F) vs. Latitude

Southern Hemisphere: Temperature (F) vs. Latitude

Northern Hemisphere: Humidity (%) vs. Latitude

Southern Hemisphere: Humidity (%) vs. Latitude

Northern Hemisphere: Cloudiness (%) vs. Latitude

Southern Hemisphere: Cloudiness (%) vs. Latitude

Northern Hemisphere: Wind Speed (mph) vs. Latitude

Southern Hemisphere: Wind Speed (mph) vs. Latitude

After each pair of plots, explain what the linear regression is modeling. Describe any relationships that you notice and any other findings you may uncover.

Your final notebook must meet the following requirements:

Randomly select at least 500 unique (not repeated) cities based on latitude and longitude.

Perform a weather check on each of the cities by using a series of successive API calls.

Include a print log of each city as it's being processed, with the city number and city name.

Save a CSV of all retrieved data and a PNG image for each scatter plot.

### ***Part 2: VacationPy***
Now, use your weather data skills to plan future vacations. Use Jupyter gmaps and the Google Places API for this part of the assignment.

>**NOTE**

Remember that any API usage beyond the $200 credit will be charged to your personal account. You can set quotas and limits to your daily requests to be sure that you won’t be charged. Check out 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Google Maps Platform Billing

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;https://developers.google.com/maps/billing/gmp-billing#monitor-and-restrict-consumption

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Manage your cost of use

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;https://developers.google.com/maps/documentation/javascript/usage-and-billing#set-caps

for more information.

To complete this part of the assignment, complete the following steps:

Create a heat map that displays the humidity for every city from Part 1, as in the following image:
heatmap

Narrow down the DataFrame to find your ideal weather condition. For example:
A max temperature lower than 80 degrees but higher than 70

Wind speed less than 10 mph

Zero cloudiness

Drop any rows that don't satisfy all three conditions. You want to be sure that the weather is ideal.
NOTE
Feel free to adjust your specifications, but make sure to set a reasonable limit to the number of rows returned by your API requests.

For each city, use the Google Places API to find the first hotel located within 5,000 meters of your coordinates.

Plot the hotels on top of the humidity heatmap, with each pin containing the Hotel Name, City, and Country, as in the following image:

hotel map

Finally, make sure to meet the following requirements:

You must complete your analysis using a Jupyter notebook.

You must use the Matplotlib or Pandas plotting libraries.

For Part 1, you must include a written description of three observable trends based on the data.

For Part 2, you must take a screenshot of the heatmap that you create and include it in your submission.

Your plots must include labeling aspects like plot title (with date of analysis) and axis labels.

For max intensity in the heatmap, try setting it to the highest humidity found in the dataset.

##  <span style="color:blue"> **Hints and Considerations** </span>
If you are having trouble displaying the maps, run jupyter nbextension enable --py gmaps in your environment and then try again.

The city data that you generate is based on random coordinates and different query times, so your outputs will not be an exact match to the provided starter notebook.

If you'd like a refresher on the geographic coordinate system, this siteLinks to an external site. has great information.

Take some time to study the OpenWeatherMap API. Based on your initial study, you should be able to answer basic questions about the API: Where do you request the API key? Which Weather API in particular will you need? What URL endpoints does it expect? What JSON structure does it respond with? Before you write a line of code, you should have a crystal-clear understanding of your intended outcome.

A starter code for citipy has been provided. However, if you're craving an extra challenge, push yourself to learn how it works by using the citipy Python libraryLinks to an external site.. Before you try to incorporate the library in your analysis, start with simple test cases outside of your main script to confirm that you are using it correctly. Often, when introduced to a new library, learners spend hours trying to figure out errors in their code when a simple test case can save you a lot of time and frustration.

You will need to apply your critical thinking skills to understand how and why we're recommending these tools. What is citipy used for? Why would you use it in conjunction with the OpenWeatherMap API? How would you do so?

While building your script, pay attention to the cities you are using in your query pool. Are you covering the full range of latitudes and longitudes? Or are you choosing 500 cities from one region of the world? Even if you were a geography genius, simply listing 500 cities based on your personal selection would create a biased dataset. Try to think of ways that you can counter these selection issues by using the full range of latitudes.

Once you have computed the linear regression for one relationship, you will follow a similar process for all other charts. As a bonus, try to create a function that will create these charts based on different parameters.

Remember that each coordinate will trigger a separate call to the Google API. If you're creating your own criteria to plan your vacation, try to reduce the results in your DataFrame to 10 or fewer cities.

Ensure that your repository has regular commits and a thorough README.md file.

Lastly, remember that this is a challenging activity. Push yourself! If you complete this task, you can safely say that you've gained a strong understanding of the core foundations of data analytics, and it will only get better from here. Good luck!

## <span style="color:indigo"> **Submission**  </span>
To submit your Challenge assignment, click Submit, and then provide the URL of your GitHub repository for grading.

>**NOTE**

You are allowed to miss up to two Challenge assignments and still earn your certificate. If you complete all Challenge assignments, your lowest two grades will be dropped. If you wish to skip this assignment, click Next, and move on to the next module.

Comments are disabled for graded submissions in Bootcamp Spot. If you have questions about your feedback, please notify your instructional staff or your Student Success Manager. If you would like to resubmit your work for an additional review, you can use the Resubmit Assignment button to upload new links. You may resubmit up to three times for a total of four submissions.

## <span style="color:Violet"> **Rubric** </span>
Module 6 Challenge Rubric

## <span style="color:Tan"> **References** </span>
© 2020 - 2022 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.