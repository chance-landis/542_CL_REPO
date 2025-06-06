# Our Information Story
We want to provide Seattle ice cream lovers with a simple interface that allows them to explore all of the city’s creameries, providing them with important information such as the address of the shops, their hours of operation, and every shop’s product offerings.
*IN SCOPE? OUT OF SCOPE?*

# Existing Information Structures

Upon research, we found existing information structures to be varied, with ice cream data stored on various sources like websites, delivery apps, or through contacting the store in person or via phone call. Because of this, there wasn't one source we could conduct a FAIR assessment of. So while the information is available for those who are searching, there isn't one good source to attain this information.

# Our Methodology: Transformation & Access
## Transformation
Since there is no existing database of Seattle ice cream shops and creameries, this
information was obtained manually. Information was collected by accessing the 
various shops’ websites, online ordering services (Doordash, Square, etc.), 
observing the store, or contacting the store for information. As information was 
gathered, it was organized in a JSON file, which was then integrated into a Flask 
app. Future maintenance will rely on users and shops submitting updated 
information, which will then be input by Cone-Quest staff on a bi-weekly basis. As 
the database grows, maintenance will occur as needed.

## Access
Users can access the information through the website or by directly interacting 
with the API. The web app will provide a friendly front-end for users looking to 
access information quickly. Through this access format, users will navigate by shop
name, then find information such as business hours, location, and flavors currently
sold under that shop name. The web interface will be best for our target users of 
ice cream lovers wishing to find information on local shops and creameries. API 
access will be focused on those who plan to use the data for other uses. Through 
the API, users will be able to make requests to access the same information without
the limitations of a web interface. This form of access will be best for direct 
access to data for any individuals who wish to use the data for non-commercial 
purposes.

### Access Instructions:

**Requirements:** Python 3, Internet Connection, Web Browser

1. Download from the GitHub repo the cone_app.py and Shop_Data.json files
2. Place the two downloaded file into the same folder on your computer
3. Install required python packages based on requirements.txt `pip install -r /path/to/requirements.txt`
4. Open the command terminal and navigate to the directory containing the downloaded files
5. In the terminal run the command `flask --app cone_app run`
6. Open the web browser and navigate to [http://127.0.0.1:5000](http://127.0.0.1:5000)
7. In the URL bar, adjust the path to receive the information you are looking for (eg. adding `/shops/names` will return all names)

## Structure
Nested JSON file that records store name, hours, address, website, flavors, 
seasonal offerings, toppings, and serving customizations (cone, cup, sizes, etc.).

## Example: *MW UPDATE NEEDED*
Request: {REQUEST_URL}/shops/names

["Frankie & Jo's University Village","Molly Moon's Homemade Ice Cream","Sweet 
Alchemy Ice Cream","Fainting Goat Gelato"]

# Performance and Quality
*DESIRED QUALITY? FINAL QUALITY? REMEDIATION PLAN?*

The desired performance of the system is to deliver responses in under 500ms (per request), 99.9% uptime and availability, and supply up-to-date information.

Currently, our system is performing other in the up-to-dateness of our information. However, due to the current size and scale of our product, we believe further testing should be conducted later to get an accurate reading.

To address our information being out of date, we plan to allow businesses to supply new and updated information directly to our service to keep our data fresh and represent the businesses accurately.

For constant alarms and monitoring, we plan to implement a pager duty alert that will throw an error if the uptime decreases past 99.9 per cent or if the response time is greater than a 500 millisecond average. Since we also want to ensure our data is fresh, we will have an alarm that verifies if the time stamps for data updates are less than 24 hours


