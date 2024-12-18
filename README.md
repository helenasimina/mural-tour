# Sources for the Madison Mural Tour:
https://madisonyoutharts.org/our-murals/
https://fox47.com/news/local restoration-underway-on-love-mural-on-side-of-williamson-st-building
https://willystreetblog.com/wp/2014/07/11/love-mural-brings-plan-b-wall-alive/
https://captimes.com/news/local/photos-love-mural-completed-at-plan-b/collection_6a3cda40-973c-5faf-8e37-0330d4a41e2d.html
https://www.revenue.wi.gov/Pages/FAQS/ise-samesex.aspx
https://www.motherfools.com/permission-wall-graffiti-mural-project
https://www.everydaymandk.com/madison-mural-tour/
https://redclovertattoocollective.com/
https://madison.bcycle.com/2021-artbikes/uw-credit-union-with-mike-lroy
https://www.facebook.com/ArtAddictsPage/videos/monarch-butterflies-street-art-mural-by-mike-lroy/717833802086241/




### _index.html_
_index.html_ contains two custom HTML parameters which allow you to change the tour basemap based on those in the Leaflet [provider's demo](https://leaflet-extras.github.io/leaflet-providers/preview/), or a custom UTL. Both are found within the `<div id='map'>`. 

`data-basemap`: Link to the basemap tiles. Default: "https://tile.openstreetmap.org/{z}/{x}/{y}.png"

`data-attribution`: Basemap attribution. Default: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'

### _stops.csv_
- _id_: The order of the stop in the tour. I.E. `1` for the first stop, `2` for the second, etc. 
- _name_: The name or title of the stop. This will appear at the top of the selected stop modal interface. 
- _audio_: The file name of an audio recording of the stop's text. Include the file type (i.e. audio.mp3). Audio recordings should be placed in the _audio_ folder.  
- _lat_: Latitude (y) of the stop location (decimal degrees).
- _lon_: Longitude (x) of the stop location (decimal degrees).
- _text_: Text content of the stop used to articulate its importance. Values in this column will be read as HTML, so you can include more complex elements and styling. 
- _direction_: Text that will appear in a popup above the stop on the map to provide user's with directions. 
- _image_: Main image that will appear below the title on the stop modal interface. Include the file type (i.e. image.png). Images should be placed in the _img_ folder.

### _route.geojson_
This geojson file contains the linestring of the tour route. Each section of the tour between two stops is a single feature. Each feature contains a single propert.
- _id_: The segment of the route on the tour. i.e. `1` for the first segment of the route.


