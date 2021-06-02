# Templates 

This subdirectory contains template CSV files for inputting supply, demand, technology site, and technology candidate data. These files can then be used for creating case studies in [ADAM.](http://54.208.179.171:8000/)

For more information on each type of file see below.

## Supply File 

The supply file contains data on the location, price, and yield of a waste product. 
For most models in ADAM, the supply of waste product is cow manure produced by Concentrated Animal Feeding Operations (CAFOs). <br>

<br>
The common headers and their descriptions are explained below: 
<br>

| Header Symbol | Description |
| ------------- | ------------- | 
| # | ID code for the supply node (i.e. name of the supply node). The name is up to user discretion. |
| Latitude | The latitude coordinate at which the node is located. <br> A **positive** number indicates **North**, and a **negative** number indicates **South**. |
| Longitude | The longitude coordinate at which the node is located. <br> A **positive** number indicates **East**, and a **negative** number indicates **West**. |
| Product ID | The product identification code that corresponds to the waste product being produced. <br>*__note: this information can be looked up in the ADAM product database.__* |
| Price | The price of the waste product in USD per product unit (e.g. USD per tonnes). <br> ***note: check the ADAM product database for product units.***  |
| Capacity | The amount of waste product produced on a time basis (e.g. 1000 tonnes per year). <br> The time basis (i.e. daily, monthy, yearly) is chosen during the first step of creating a new model in ADAM.  <br> *__note: check the ADAM product database for product units.__* |

<br>


Here is how it would look in a supply file used in ADAM: 

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| s1 | 43.0731 | -89.4012 | p5 | 0 | 500 |
| ...  | ... | ...  | ... | ...  | ... |

Using these information, we can interpert the entry in the example above as a supply node (which is denoted "s1" for simplicity) located at 43.0731 N, 89.4012 W which produces 
liquid digestate waste product (p5) at a yield of 500 tonnes per time basis and at zero cost to the supplier.  
**Remember:** time is defined on the first step of creating a model in ADAM, so there is no way to know the time basis from the supply file alone.

<br>
Now try to interpert this example supply file on your own: 

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| ...  | ... | ...  | ... | ...  | ... |
| s5 | 39.7687 | -76.6797 | p25 | 0.06 | 1200 |
| ...  | ... | ...  | ... | ...  | ... |

<details> 
  <summary>Check your answer here.</summary>
  Supply node s5 is located at 39.7687 N, 76.6797 W which produces Biogas (60% CH4) at a yield of 1200 cubic meters per time basis, at a cost of 0.06 USD per cubic meter.  
</details>
<br>

## Demand File 

The demand data file contains information about the nodes that demand

The template demand file will look similar to the example below: 

| # | Latitude | Longitude | Product ID | Price | Capacity |
| ------------- | ------------- | ------------- | ------------- | ------------- | ------------- |
| d1 | 43.0731 | -89.4012 | p2 | 0.06 | 1200 |
| ...  | ... | ...  | ... | ...  | ... |


