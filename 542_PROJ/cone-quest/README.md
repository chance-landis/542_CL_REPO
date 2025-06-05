## About
Cone-Quest is a web page ice cream lovers can turn to in order to find detailed 
information about ice cream parlors and creameries in the greater Seattle area. 
Information is collected from various shops in the area and compiled into one 
source of information ice cream lovers can use to find the right cold treat they 
are looking for. 

## Methodology
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

## Structure
Nested JSON file that records store name, hours, address, website, flavors, 
seasonal offerings, toppings, and serving customizations (cone, cup, sizes, etc.).

## Example
Request: {REQUEST_URL}/shops/names
["Frankie & Jo's University Village","Molly Moon's Homemade Ice Cream","Sweet 
Alchemy Ice Cream","Fainting Goat Gelato"]
