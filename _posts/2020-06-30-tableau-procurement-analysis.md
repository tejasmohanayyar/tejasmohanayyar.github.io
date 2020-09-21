---
layout: post
title: "A procurement analysis of inventory"
permalink: "tableau-procurement-analysis"

---
|Inventory by category|Inventory by product|
|---|---|
|<img src="/images/tableau-images/proc5.png">|<img src="/images/tableau-images/proc6.png">|

#### About the data:

Supply chain data of a company that shows purchased goods with detailed information about various parameters.

|Column|Measure/Dimension|
|---|---|
|Category|Dimension|
|Committed|Measure|	
|Jan demand|Measure|
|Location|Dimension|	
|Max|Measure|
|Min|Measure|
|Number of Records|Measure|
|On PO|Measure|
|On hand|Measure|
|Product Name|Dimension|
|SS|Measure|
|Sub- Category|Dimension|
Unit Cost|Measure|
|Unit Price|Measure|
|Concat|Dimension|
|On Hand|Measure|
|Order 1|Measure|
|Order|Measure|

#### Analyzing the data:

* Find the inventory by :-

  1. Category
  2. Sub Category
  3. Product
  4. Location

* Create a Dashboard

* Create a story showing the visuals from Location, Product & Category

#### Category:

<img src = "/images/tableau-images/proc1.png">

##### Procedure followed:

* Dragged Category into columns field.
* Dragged On Hand as SUM measure into rows field.
* Created a field called On Hand $ = On Hand * Unit Price.
* Dragged created field to marks section as SUM and changed type to text. 
* Added table calculation as percent of total.
* Chose Bar chart to show comparison between inventories.

#### Sub-Category:

<img src = "/images/tableau-images/proc2.png">

##### Procedure followed:

* Dragged sub-category dimension into columns field.
* Dragged on hand as SUM into row field.
* Added on hand $ field into marks as sum.
* Added table calculation to on hand $ as % of total.
* Selected bar chart.


#### Product:

<img src = "/images/tableau-images/proc3.png">

##### Procedure followed:

* Dragged Product name dimension to columns field.
* Dragged on hand as SUM into row field.
* Selected bar chart.

#### Location:

<img src = "/images/tableau-images/proc4.png">

##### Procedure followed:

* Dragged location into marks field. Automatically latitude and longitude were selected into rows and columns field respectively.
* Next selected On hand $ and changed type to color.

#### Creating a dashboard for *inventory by category*.

<img src="/images/tableau-images/proc5.png">

##### Procedure followed:

* After creating all our visuals we would now create a dashboard based on our requirements.
* Drag the Inventory by location visual created into the dashboard.
* Next drag the inventory by category visual into the dashboard.
* The dash board allows us to see inventory by category for each location letting us drill down into specific details.

#### Creating a dashboard for *Inventory by product*.

<img src="/images/tableau-images/proc6.png">

##### Procedure followed:

* Similar to the previous dashboard but the only change is that instead of the product category visual we drag in the Inventory by product visual. 
* The functionality is same as the above dashboard.

#### Creating a story showing the visuals from Location, Product & Category:

|Storypoint1|StoryPoint2|
|---|---|
|<img src = "/images/tableau-images/procstory1.png">|<img src = "/images/tableau-images/procstory2.png">|

##### Procedure followed:

* Created a new story point for each dashboard.
* This allows us to present the data in a seemless manner.
* We first look at inventory by category for each location.
* Then we drill into the data to look at inventory for each product by location making a seemless transition between the two.

#### Conclusion:

* Technology has the highest inventory value in the companies warehouses.
* Copiers seem to be their prime source of business since it makes up a large chunk of the companies inventory value.
* To be more specific the Canon PC940 copier has the highest value in terms of inventory.
* New Mexico is currently holding the largest amount of inventory.


#### Project Files:

Please find the project files <a target = "_blank" href = "https://github.com/tejasmohanayyar/tejasmohanayyar.github.io/tree/master/projects/tableau-projects/Procurement%20Spend%20Analysis">here</a>.
