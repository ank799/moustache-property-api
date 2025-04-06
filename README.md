# moustache-property-api
# Assignment Overview

> **NOTE:** Please note that you are free to use the tools and helpers of your choice for the final objective to be met, but the code and application should be built on either of Go or Python.
> 

We are serving a business called Moustache Escapes(https://www.moustachescapes.com/) where you are building API’s for assisting their tele-calling team when they are having a conversation with customers regarding their hotel rooms and properties. 

Customers call from various parts of the country, and customers would want to visit the city where they have hotels, or nearby areas/cities.

In order to ensure that they convert most calls to customers, they require to know the distance of the location mentioned by the customer and find the nearest property that is available. If the property is in the 50km range of the location mentioned by the person, the location should be shown to the tele-calling agent.

You are required to create a backend service which would consider the constraints and core requirements to build an API which would be utilized by the team to create the application for showing the nearest property. The only input that you would receive would be the query entered by the tele-calling agent, while the output would be the list of properties that are available in the 50km radius of the location mentioned. If there are no properties available, the API should return the same.
**Core Requirements:**

- With the input coming in as a query ( any city, state, or area in the country ) you are required to output the list of properties that are in the radius of 50km.
- If there are no properties available, then output the same.
- You are required to only build the backend API and no frontend is required.
- You are free to use LLMs and any tools such as Sambanova, OpenAI, Groq, etc. and any python or GO libraries that you seem necessary.

**Technical Constraints:**

- The response time of the API should be less than 2 seconds as the tele-caller would be using this for real-time communication.
- Due to the tele-calling typing fast, there might be spelling mistakes which might come as input ( delhi → delih, bangalore → bangalre ). The spelling mistakes would be constraint to 1 or 2 missing characters, or the characters getting swapped.

**Assumptions:**

- The input would only be for areas, cities and states and not landmarks and buildings for proximity.
- The distance calculated based on the latitude and longitude would be the correct distance.

### Example Input:

1. Sissu
    1. Sissu is a town in Himachal Pradesh, so the nearest properties would be the property in Koksar which is approximately 5KM away. ( real number calculated based on the latitude and longitude )
    *Output: Nearest property is Koksar which is 5KM away* 
2. Jaipur
    1. Moustache has a property in Jaipur, so the output would mention the same.
