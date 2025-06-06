# Our Information Story
We want to provide Seattle ice cream lovers with a simple interface that allows them to explore all of the city’s creameries, providing them with important information such as the address of the shops, their hours of operation, and every shop’s product offerings.
*IN SCOPE? OUT OF SCOPE?*

# Existing Information Structures
*FAIR ASSESSMENT? TRANSFORMATIONS NEEDED?*

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

1. Download from the GitHub repo the Flask.py and Shop_Data.json files
3. 

## Structure
Nested JSON file that records store name, hours, address, website, flavors, 
seasonal offerings, toppings, and serving customizations (cone, cup, sizes, etc.).

## Example: *MW UPDATE NEEDED*
Request: {REQUEST_URL}/shops/names

["Frankie & Jo's University Village","Molly Moon's Homemade Ice Cream","Sweet 
Alchemy Ice Cream","Fainting Goat Gelato"]

# Performance and Quality
*DESIRED QUALITY? FINAL QUALITY? REMEDIATION PLAN?*
