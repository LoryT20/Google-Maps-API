# User-s-Guide
To open the completed code, go to the following URL
http://jsfiddle.net/LoryT20j/s2h9d59a/528/

Alternatively, you can copy and paste the code to the segments that correspond to the file name. Additionally, you would have to copy and paste these links into resources
https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.8.0/xlsx.full.min.js
https://rawgit.com/kanghj/alasql/xls_browser_import/dist/alasql.js

To run the code on JsFiddle, click ‘run’ near the top left corner, then click ‘choose file’ from the box on the lower right corner. select the file you wish to open. If there are two columns named ‘location’ and ‘state’, and the contents of those segments contain the names of real cities and states, the location(s) should be plotted onto the map.

HTML explained:
the first line utilizes the AlaSQL database, allowing the user to access local files. The data from these files will be sent over to the lodeFile method under the variable name 'event'. The next 3 lines are to set up the map

CSS explained:
This segment simply sets up how the map will be displayed: height, width, margins, etc.

Body explained:
The first line sets up the first method, with the data from the chosen file being resembled by the perimeter variable, 'event'. The next 3 lines are to set up the contents of the map. Specifically, the default center and zoom. Currently, the map is set to center into the United States. Lines 6-12 goes over the collected data from ‘event’ almost like a 2D array. It will look for the columns labeled 'Location' and 'State'. It will then create a string variable to resemble a city and state address. Through lines 13-26, a tool called geocoder is used to collect information from said string. It essentially seems to work as if you searched it from google itself. From there, we can collect its coordinates and plot them onto the map. I created a loop to repeat this process for every row containing a location and state.
