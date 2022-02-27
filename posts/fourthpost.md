---
title: API Back End Wikipedia-Query Tag Creation
description: This is a post on My Blog about wikipedia-query tag creation
date: 2022-01-30
tags: second tag
layout: layouts/post.njk
---
This posting will be about the usage of an IP address, using longitude and latitude to get a Google Maps iframe, and using this information in tandem with a wikipedia-query tag.  I will also be discussing _fetch_ as well _LitElements_ to provide insight into updating of the DOM.

## The GeoIP Element

The [GeoIP] (https://freegeoip.app) element is an API.  It allows programmers to retrieve data from a user's IP address.  This data could include the following: 

![pieces of geoip](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kq16s1mtuivujz0rw7y8.png)

For my work, I used the GeoIP API to retrieve the user's longitude, latitude, city, and state. 

##Google Maps: iframe
The Google Maps iframe takes in a latitude and longitude in order to display a map.  The latitude and the longitude stem from the user's IP address.  Therefore, the usage of the GeoIP API is necessary to successfully display the iframe.  

<u>Step by step instructions for implementation: </u>

1. In the constructor you must set your locationEndpoint.  You can do so by entering: `this.locationEndpoint = 'https://freegeoip.app/json/'`.  The **locationEndpoint** is what is going to allow for a connection to the necessary software.
2. Within your properties, add the following: 
![properties](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/z6x893yylccgzcdgrft5.png)
The property named **long** will be used for longitude, the property **lat** for latitude, **city** for the user's city, and finally **region** for the user's state.
3. The next step has you assigning values to the properties that you declared.  This step is what ensures that the user's data is correctly outputted.  Enter the code as follows: 

![geoipProp](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/mi6fjnjn1k3q3j9287ut.png)
4. Now you can begin rendering your map!  The first thing you want to do in order to render is create a `const url` that will work with the properties that you declared.  Based on this example, therefore, the url would be: 
`https://maps.google.com/mapsq=${this.lat},${this.long}&t=&z=15&ie=UTF8&iwloc=&output=embed`.  The interchangeable parts are **${this.lat}** and **${this.long}**.  These could be substituted for corresponding property names, as long as they refer to longitude and latitude. 
5. The creation of the iframe is going to rely on the url that was made in step 4.  To make the iframe, simply type: `html <iframe title = "Location" src="${url}"></iframe> `.  The **title** can be changed based on preference, but the **src** must be the url that you specified from step 4. 

##Wikipedia-query Tag
In order to successfully wire information into a Wikipedia-query tag, the previous steps must be completed as well as the following: 

1. **Dependencies and Import**:  If you would like your Wikipedia-query to work make sure to add the following import to your application: `import '@lrnwebcomponents/wikipedia-query/wikipedia-query.js';`.  After you have added this import, navigate to your terminal (make sure you have run the proper cd into your directory) and run `npm install` and once that process has finished run `npm start`.  To check that the proper dependencies were added, in your IDE navigate to the **package.json** file.  Here, you should see a section titled "Dependencies".  Under this section, search for the following:
`"@lrnwebcomponents/meme-maker": "^4.0.6",
    "@lrnwebcomponents/wikipedia-query": "^4.0.6",`.  if you are able to locate these, the import and dependencies are functional.
2. You can now create the Wikipedia-query tag in your rendering function.  For this example, I was able to complete this action by entering the following: 

![querying](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/8y0k8pfazyusrfd7fax8.png)

Again, the `this.region` will refer to the user's state and the `this.city` to the user's city.  This tag will render an embedded Wikipedia article!

##Fetch and LitElement
How can `fetch` be used to gain information from the API?
In practice, fetch is used to asynchronously receive resources across the network.  
In my example, I used `fetch` to complete the following task: 

![fetch](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kog3aqycodil5cp4pdy5.png)

This excerpt from my code is using information from the **locationEndpoint** and **userIPData.ip** to print data to the console. 

`Fetch` is used with `LitElement` to provide updating of the DOM by ensuring that the console logs that proper user data. 

##Sources
[GeoIP] (https://freegeoip.app)
[API Endpoint Explanation]
(https://www.techtarget.com/searchapparchitecture/definition/API-endpoint)
[Wikipedia Tag Example](https://codepen.io/btopro/pen/yLNmVbw)
[Fetch Explanation]
(https://developer.mozilla.org/enUS/docs/Web/API/Fetch_API/Using_Fetch)


##My Source Code
https://github.com/TaylorMorini/ip-project

