# INF 554 Final Presentation


## Slide 1 - Cover
#### Group name: Eureka
#### Project name: Metro Bike Sharing
#### Group member:  
* Yiran Li - liyiran@usc.edu
* Xiner Ning - xinernin@usc.edu
* Yueqin Yang - yueqinya@usc.edu
#### Link to Public Webpage:
- [Metro Bike Sharing](http://www-scf.usc.edu/~liyiran/final/)

## Slide 2 - What our visualization is about?
- To show does the metro bike station set properly? 
- Does it need more stations in some regions?

## Slide 3 -  who is it addressed to?
- Bike rental company
- Professor, TA

## Slide 4 - Why it is interesting, original, useful?
- New market
- Close to our daily life
- New area no research before
- Enough data and authentic

## Slide 5 - Work distribution
- Yiran: framework and maps
- Xiner: navigation and charts
- Yueqin: data and charts

## Slide 6 - Explain that data and topic as needed to understand the project
- we use a d3 map to show the combination of bike stations, public transportations, to show whether we need add stations in some new regions
- we use the bar charts to show the usage for existing stations, to show whether we need add more docks for those existing stations

## Slide 7 - Researchs
- Metro bike website
- vue
- bootstrop
- professor examples

## Slide 8 - What others have done in the same topic, other topics that are relevant?
- Our project is NOT groundless. We stand on the shoulders of giants. After doing search some research, we find that our project is very unique. 
We list the current research for sharing economy
- ofo / mobike - no satisfiable visualizations
- Car-sharing e.g. Car-to-go real time info / chromatic data analysis
- Metro bike existing visualization only has few dimensions / multi-charts

## Slide 9, Slide 10 - MAP
 To optimize the visual queries, we try to make the interaction as simple and intuitive as possible. 
 Once the user clicks a station on the map, the all charts will be changed to show the details because the mapbox sends an event to the sub components. 
 The dropdown list can also send the event to the pie chart to show the information.
 As user move the cursor over the graph, the corresponding component will also be changed. All interactions are quite popular and well known. We do not invent any new gestures.
 In the website, we apply [Model-View-Presenter](https://en.wikipedia.org/wiki/Model–view–presenter) architecture. _HTML_ and _CSS_ will take care of **View** while _Javascript_ is for **Model** and **View**.

 
## Slide 11 & 12 - Pie chart
- Bike usage distribution: average bike used of each region in every month
- `d3.pie()`
- Dropdown box to select month
- Interactive information card
- Mouseover pop out effect

## Slide 13 - Line chart
- Bike usage trend along months: bike usage in summer months is significantly higher than winter months
- `d3.line()`
- Resposive
- Mouseover pop out effect



## Slide 14 - Design process
In order to work in parallel, we have divided our website into several components, e.g. Dot map in D3, mapbox map, line charts etc. 
After having those components defined, each team member takes one or more components. Technically speaking, each component are in MVC structure. For view part, we use bootstrap to make the basic layout responsive.
However, it is not sufficient since we also want to change the size of the chart correspondingly. To achieve that, we need to use our controller to redraw the graph, which will be explained later.
In order to make our layout clearly, we put the general information on the top of the page and the details are below the general information. The colors of the graphs are also well considered. 
We try to make the color as clear as possible.

The main job of the controller is to draw the graph and adjust the graphs based on the size of the window. Once the user clicks an object, the GUI will send a event to the event bus that can reduce the coupling between the conponents.
Following that, the components can be invoked by the event bus and refresh the UI.   


## Slide 15 - What would you done differently?
After doing some research, we have found the most of the current reports are based on Google map, which is highly coupling to Google service. However, we decide to use D3 to draw our map which can save tons of traffic and 
make cache perform much better.
**Week** | **Plan**
--- | ---
Week 5 | topic choosing / requirement analysis 
Week 6 | framework / prototype on whiteboard / proposal presentation
Week 7 | Excel prototype / feature engineering
Week 8 | Excel prototype / feature engineering
Week 9 | workload distribution / implementation
Week 10 | implementation
Week 11 | implementation
Week 12 | integration 
Week 13 | paper working / summarizing
Week 14 | final webpage / video / final presentation

## Authors
- Yiran Li
- Yueqin Yang 
- Xiner Ning