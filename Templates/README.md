# Templates 

This subdirectory contains template CSV files for inputting supply, demand, technology site, and technology candidate data. These files can then be used for creating case studies in [ADAM](http://54.208.179.171:8000/)

## Supply File 

The supply file contains data on the location, price, and yield of a waste product. 
For models in ADAM, the supply of waste product is cow manure produced by Concentrated Animal Feeding Operations (CAFOs). <br>

The template supply file will look similar to the example below: 

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| s1 | 43.835418 | -88.293544 | p5 | 0 | 1000 |
| ...  | ... | ...  | ... | ...  | ... |


| Header Symbol | Description |
| ------------- | ------------- | 
| **#** | This is the name of the supply node |
| **Latitude** | The latitude coordinate at which the node is located |
| Longitude | The longitude coordinate at which the node is located |
| Product ID | The product identification code which corresponds to the waste product being produced. This innformation can be looked up in the ADAM product database. |
| Price | The price of the waste product |
| Capacity | The amount of waste product produced on a time basis (i.e. 1000 tonnes per year) |



